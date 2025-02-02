---
UID: NF:ntifs.FsRtlDissectName
title: FsRtlDissectName function (ntifs.h)
description: Given a Unicode pathname string, the FsRtlDissectName routine returns two strings, one containing the first file name found in the string, the other containing the remaining unparsed portion of the pathname string.
old-location: ifsk\fsrtldissectname.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FsRtlDissectName function"]
ms.keywords: FsRtlDissectName, FsRtlDissectName routine [Installable File System Drivers], fsrtlref_a74da803-0994-46e4-90f7-bc7728b59fe5.xml, ifsk.fsrtldissectname, ntifs/FsRtlDissectName
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
ms.custom: RS5
f1_keywords:
 - FsRtlDissectName
 - ntifs/FsRtlDissectName
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - FsRtlDissectName
dev_langs:
 - c++
---

# FsRtlDissectName function


## -description

Given a Unicode pathname string, the <b>FsRtlDissectName</b> routine returns two strings, one containing the first file name found in the string, the other containing the remaining unparsed portion of the pathname string.

## -parameters

### -param Path [in]


Pathname string to be parsed.

### -param FirstName [out]


Pointer to the first file name in the pathname string.

### -param RemainingName [out]


Pointer to the remaining unparsed portion of the pathname string.

## -remarks

In the input string, backslashes are read as name separators. The first name in the string is assumed to consist of all characters from the beginning of the string to the character preceding the first backslash, inclusive. There is just one exception to this rule: if the first character in the input string is a backslash, this character is ignored and does not appear in the output string. The remaining portion of the string consists of all characters following the backslash that follows the first name found in the string.

<b>FsRtlDissectName</b> does not check for the presence of illegal characters in the input string.

The following table shows sample input and output values for <b>FsRtlDissectName</b>.  

<table>
<tr>
<th>Path</th>
<th>FirstName</th>
<th>RemainingName</th>
</tr>
<tr>
<td>
empty

</td>
<td>
empty

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A

</td>
<td>
A

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A\B\C\D\E

</td>
<td>
A

</td>
<td>
B\C\D\E

</td>
</tr>
<tr>
<td>
*A?

</td>
<td>
*A?

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
\A

</td>
<td>
A

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A[,]

</td>
<td>
A[,]

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A\\B+;\C

</td>
<td>
A

</td>
<td>
\B+;\C

</td>
</tr>
</table>
 

Note that upon returning, the <b>Buffer</b> members of the output parameters will point into the <b>Buffer</b> member of <b>Path</b>.  Therefore, the caller should not allocate storage for the <b>Buffer</b> members of the two output parameters, as shown in the following example:


```
.
.
.
/*
The FsRtlDissectName routine will set the members
of the following two structures appropriately:
*/
UNICODE_STRING CurrentComponent;
UNICODE_STRING RemainingComponent;

/*
Do not allocate storage for the Buffer members of CurrentComponent
and RemainingComponent in that they will point into the previously
allocated storage of FullPathName's Buffer member:
*/
FsRtlDissectName (FullPathName, &CurrentComponent, &RemainingComponent);
.
.
.
```

For information about other string-handling routines, see <a href="/windows-hardware/drivers/ddi/_kernel/#run-time-library-rtl-routines">Run-Time Library (RTL) Routines</a>.

## -see-also

<a href="/windows/win32/api/ntdef/ns-ntdef-_unicode_string">UNICODE_STRING</a>
