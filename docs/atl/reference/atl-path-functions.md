---
title: "ATL Path functions | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.topic: "reference"
helpviewer_keywords: ["ATL, path"]
f1_keywords: ["ATLPATH/ATL::ATLPath::AddBackslash", "ATLPATH/ATL::ATLPath::AddExtension", "ATLPATH/ATL::ATLPath::Append", "ATLPATH/ATL::ATLPath::BuildRoot", "ATLPATH/ATL::ATLPath::Canonicalize", "ATLPATH/ATL::ATLPath::Combine", "ATLPATH/ATL::ATLPath::CommonPrefix", "ATLPATH/ATL::ATLPath::CompactPath", "ATLPATH/ATL::ATLPath::CompactPathEx", "ATLPATH/ATL::ATLPath::FileExists", "ATLPATH/ATL::ATLPath::FindExtension", "ATLPATH/ATL::ATLPath::FindFileName", "ATLPATH/ATL::ATLPath::GetDriveNumber", "ATLPATH/ATL::ATLPath::IsDirectory", "ATLPATH/ATL::ATLPath::IsFileSpec", "ATLPATH/ATL::ATLPath::IsPrefix", "ATLPATH/ATL::ATLPath::IsRelative", "ATLPATH/ATL::ATLPath::IsRoot", "ATLPATH/ATL::ATLPath::IsSameRoot", "ATLPATH/ATL::ATLPath::IsUNC", "ATLPATH/ATL::ATLPath::IsUNCServer", "ATLPATH/ATL::ATLPath::IsUNCServerShare", "ATLPATH/ATL::ATLPath::MakePretty", "ATLPATH/ATL::ATLPath::MatchSpec", "ATLPATH/ATL::ATLPath::QuoteSpaces", "ATLPATH/ATL::ATLPath::RelativePathTo", "ATLPATH/ATL::ATLPath::RemoveArgs", "ATLPATH/ATL::ATLPath::RemoveBackslash", "ATLPATH/ATL::ATLPath::RemoveBlanks", "ATLPATH/ATL::ATLPath::RemoveExtension", "ATLPATH/ATL::ATLPath::RemoveFileSpec", "ATLPATH/ATL::ATLPath::RenameExtension", "ATLPATH/ATL::ATLPath::SkipRoot", "ATLPATH/ATL::ATLPath::StripPath", "ATLPATH/ATL::ATLPath::StripToRoot", "ATLPATH/ATL::ATLPath::UnquoteSpaces"]
ms.assetid: d1ec2b8d-7ec7-43ea-90dd-0a740d2a742b
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus"]
---
# ATL Path functions

ATL provides the ATLPath class for manipulating paths in the form of [CPathT](cpatht-class.md). This code can be found in atlpath.h.  
  
### Related Classes  
  
|||  
|-|-|  
|[CPathT Class](cpatht-class.md)|This class represents a path.|  

### Related Typedefs  
  
|||  
|-|-|  
|`CPath`|A specialization of [CPathT](cpatht-class.md) using `CString`.|  
|`CPathA`|A specialization of [CPathT](cpatht-class.md) using `CStringA`.|  
|`CPathW`|A specialization of [CPathT](cpatht-class.md) using `CStringW`.|  
  
### Functions  
  
|||  
|-|-|  
|[ATLPath::AddBackslash](#addbackslash)|This function is an overloaded wrapper for [PathAddBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773561).|  
|[ATLPath::AddExtension](#addextension)|This function is an overloaded wrapper for [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563).|  
|[ATLPath::Append](#append)|This function is an overloaded wrapper for [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565).|  
|[ATLPath::BuildRoot](#buildroot)|This function is an overloaded wrapper for [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567).|  
|[ATLPath::Canonicalize](#canonicalize)|This function is an overloaded wrapper for [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569).|  
|[ATLPath::Combine](#combine)|This function is an overloaded wrapper for [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571).|  
|[ATLPath::CommonPrefix](#commonprefix)|This function is an overloaded wrapper for [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574).|  
|[ATLPath::CompactPath](#compactpath)|This function is an overloaded wrapper for [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575).|  
|[ATLPath::CompactPathEx](#compactpathex)|This function is an overloaded wrapper for [PathCompactPathEx](http://msdn.microsoft.com/library/windows/desktop/bb773578).|  
|[ATLPath::FileExists](#fileexists)|This function is an overloaded wrapper for [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584).|  
|[ATLPath::FindExtension](#findextension)|This function is an overloaded wrapper for [PathFindExtension](http://msdn.microsoft.com/library/windows/desktop/bb773587).|  
|[ATLPath::FindFileName](#findfilename)|This function is an overloaded wrapper for [PathFindFileName](http://msdn.microsoft.com/library/windows/desktop/bb773589).|  
|[ATLPath::GetDriveNumber](#getdrivenumber)|This function is an overloaded wrapper for [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612).|  
|[ATLPath::IsDirectory](#isdirectory)|This function is an overloaded wrapper for [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621).|  
|[ATLPath::IsFileSpec](#isfilespec)|This function is an overloaded wrapper for [PathIsFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773627).|  
|[ATLPath::IsPrefix](#isprefix)|This function is an overloaded wrapper for [PathIsPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773650).|  
|[ATLPath::IsRelative](#isrelative)|This function is an overloaded wrapper for [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660).|  
|[ATLPath::IsRoot](#isroot)|This function is an overloaded wrapper for [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674).|  
|[ATLPath::IsSameRoot](#issameroot)|This function is an overloaded wrapper for [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687).|  
|[ATLPath::IsUNC](#isunc)|This function is an overloaded wrapper for [PathIsUNC](http://msdn.microsoft.com/library/windows/desktop/bb773712).|  
|[ATLPath::IsUNCServer](#isuncserver)|This function is an overloaded wrapper for [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722).|  
|[ATLPath::IsUNCServerShare](#isuncservershare)|This function is an overloaded wrapper for [PathIsUNCServerShare](http://msdn.microsoft.com/library/windows/desktop/bb773723).|  
|[ATLPath::MakePretty](#makepretty)|This function is an overloaded wrapper for [PathMakePretty](http://msdn.microsoft.com/library/windows/desktop/bb773725).|  
|[ATLPath::MatchSpec](#matchspec)|This function is an overloaded wrapper for [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727).|  
|[ATLPath::QuoteSpaces](#quotespaces)|This function is an overloaded wrapper for [PathQuoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773739).|  
|[ATLPath::RelativePathTo](#relativepathto)|This function is an overloaded wrapper for [PathRelativePathTo](http://msdn.microsoft.com/library/windows/desktop/bb773740).|  
|[ATLPath::RemoveArgs](#removeargs)|This function is an overloaded wrapper for [PathRemoveArgs](http://msdn.microsoft.com/library/windows/desktop/bb773742).|  
|[ATLPath::RemoveBackslash](#removebackslash)|This function is an overloaded wrapper for [PathRemoveBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773743).|  
|[ATLPath::RemoveBlanks](#removeblanks)|This function is an overloaded wrapper for [PathRemoveBlanks](http://msdn.microsoft.com/library/windows/desktop/bb773745).|  
|[ATLPath::RemoveExtension](#removeextension)|This function is an overloaded wrapper for [PathRemoveExtension](http://msdn.microsoft.com/library/windows/desktop/bb773746).|  
|[ATLPath::RemoveFileSpec](#removefilespec)|This function is an overloaded wrapper for [PathRemoveFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773748).|  
|[ATLPath::RenameExtension](#renameextension)|This function is an overloaded wrapper for [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749).|  
|[ATLPath::SkipRoot](#skiproot)|This function is an overloaded wrapper for [PathSkipRoot](http://msdn.microsoft.com/library/windows/desktop/bb773754).|  
|[ATLPath::StripPath](#strippath)|This function is an overloaded wrapper for [PathStripPath](http://msdn.microsoft.com/library/windows/desktop/bb773756).|  
|[ATLPath::StripToRoot](#striptoroot)|This function is an overloaded wrapper for [PathStripToRoot](http://msdn.microsoft.com/library/windows/desktop/bb773757).|  
|[ATLPath::UnquoteSpaces](#unquotespaces)|This function is an overloaded wrapper for [PathUnquoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773763).|  
  
## Requirements  
 **Header:** atlpath.h  

## <a name="addbackslash"></a> ATLPath::AddBackSlash

This function is an overloaded wrapper for [PathAddBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773561).  
  
### Syntax  
  
```  
inline char* AddBackslash(char* pszPath);  
inline wchar_t* AddBackslash(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathAddBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773561) for details.  
  
 
  

## <a name="addextension"></a> ATLPath::AddExtension
 This function is an overloaded wrapper for [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563).  
  
### Syntax  
  
```  
inline BOOL AddExtension(char* pszPath, const char* pszExtension);  
inline BOOL AddExtension(wchar_t* pszPath, const wchar_t* pszExtension);  
```  
  
### Remarks  
 See [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563) for details. 
  
## <a name="append"></a> ATLPath::Append
 This function is an overloaded wrapper for [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565).  
  
### Syntax  
  
```  
inline BOOL Append(char* pszPath, const char* pszMore);  
inline BOOL Append(wchar_t* pszPath, const wchar_t* pszMore);  
```  
  
### Remarks  
 See [PathAppend](http://msdn.microsoft.com/library/windows/desktop/bb773565) for details.  
  
 
  

## <a name="buildroot"></a> ATLPath::BuildRoot
 This function is an overloaded wrapper for [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567).  
  
### Syntax  
  
```  
inline char* BuildRoot(char* pszPath, int iDrive);  
inline wchar_t* BuildRoot(wchar_t* pszPath, int iDrive);  
```  
  
### Remarks  
 See [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567) for details.  
  
 
  

## <a name="canonicalize"></a> ATLPath::Canonicalize
 This function is an overloaded wrapper for [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569).  
  
### Syntax  
  
```  
inline BOOL Canonicalize(char* pszDest, const char* pszSrc);  
inline BOOL Canonicalize(wchar_t* pszDest, const wchar_t* pszSrc);  
```  
  
### Remarks  
 See [PathCanonicalize](http://msdn.microsoft.com/library/windows/desktop/bb773569) for details.  
  
 
  

## <a name="combine"></a> ATLPath::Combine 
This function is an overloaded wrapper for [PathCombine](https://msdn.microsoft.com/library/windows/desktop/bb773571).  

### Syntax  
```
inline char* Combine(  
   char* pszDest,
   const char* pszDir,
   const char* pszFile 
);

inline wchar_t* Combine(  
   wchar_t* pszDest,
   const wchar_t* pszDir,
   const wchar_t* pszFile);
```
### Remarks
See PathCombine for details.


## <a name="commonprefix"></a> ATLPath::CommonPrefix
 This function is an overloaded wrapper for [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574).  
  
### Syntax  
  
```  
inline int CommonPrefix(  
   const char* pszFile1, 
   const char* pszFile2,  
   char* pszDest);  

inline int CommonPrefix(  
   const wchar_t* pszFile1,  
   const wchar_t* pszFile2,  
   wchar_t* pszDest);  
```  
  
### Remarks  
 See [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574) for details.  
  
 
  

## <a name="compactpath"></a> ATLPath::CompactPath
 This function is an overloaded wrapper for [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575).  
  
### Syntax  
  
```  
inline BOOL CompactPath(  
   HDC hDC,  
   char* pszPath,  
   UINT dx);  

inline BOOL CompactPath(  
   HDC hDC,  
   wchar_t* pszPath,  
   UINT dx);  
```  
  
### Remarks  
 See [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575) for details.  
  
 
  

## <a name="compactpathex"></a> ATLPath::CompactPathEx
 This function is an overloaded wrapper for [PathCompactPathEx](http://msdn.microsoft.com/library/windows/desktop/bb773578).  
  
### Syntax  
  
```  
inline BOOL CompactPathEx(  
   char* pszDest,  
   const char* pszSrc,  
   UINT nMaxChars,  
   DWORD dwFlags);  

inline BOOL CompactPathEx(  
   wchar_t* pszDest,  
   const wchar_t* pszSrc,  
   UINT nMaxChars,  
   DWORD dwFlags);  
```  
  
### Remarks  
 See [PathCompactPathEx](http://msdn.microsoft.com/library/windows/desktop/bb773578) for details.  
  
 
  

## <a name="fileexists"></a> ATLPath::FileExists
 This function is an overloaded wrapper for [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584).  
  
### Syntax  
  
```  
inline BOOL FileExists(const char* pszPath);  
inline BOOL FileExists(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathFileExists](http://msdn.microsoft.com/library/windows/desktop/bb773584) for details.  
  
 
  

## <a name="findextension"></a> ATLPath::FindExtension
 This function is an overloaded wrapper for [PathFindExtension](http://msdn.microsoft.com/library/windows/desktop/bb773587).  
  
### Syntax  
  
```  
inline char* FindExtension(const char* pszPath);  
inline wchar_t* FindExtension(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathFindExtension](http://msdn.microsoft.com/library/windows/desktop/bb773587) for details.  
  
 
  

## <a name="findfilename"></a> ATLPath::FindFileName
 This function is an overloaded wrapper for [PathFindFileName](http://msdn.microsoft.com/library/windows/desktop/bb773589).  
  
### Syntax  
  
```  
inline char* FindFileName(const char* pszPath);  
inline wchar_t* FindFileName(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathFindFileName](http://msdn.microsoft.com/library/windows/desktop/bb773589) for details.  
  
 
  

## <a name="getdrivenumber"></a> ATLPath::GetDriveNumber  
 This function is an overloaded wrapper for [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612).  
  
### Syntax  
  
```  
inline int GetDriveNumber(const char* pszPath);  
inline int GetDriveNumber(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612) for details.  
  
 


## <a name="isdirectory"></a>  ATLPath::IsDirectory 
This function is an overloaded wrapper for [PathIsDirectory](https://msdn.microsoft.com/library/windows/desktop/bb773621).

```  
inline BOOL IsDirectory(const char* pszPath);
inline BOOL IsDirectory(const wchar_t* pszPath);
```  
### Remarks
See PathIsDirectory for details.  

## <a name="isfilespec"></a> ATLPath::IsFileSpec
 This function is an overloaded wrapper for [PathIsFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773627).  
  
### Syntax  
  
```  
inline BOOL IsFileSpec(const char* pszPath);  
inline BOOL IsFileSpec(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773627) for details.  
  
 
  

## <a name="isprefix"></a> ATLPath::IsPrefix
 This function is an overloaded wrapper for [PathIsPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773650).  
  
### Syntax  
  
```  
inline BOOL IsPrefix(const char* pszPrefix, const char* pszPath);  
inline BOOL IsPrefix(const wchar_t* pszPrefix, const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773650) for details.  
  
 
  

## <a name="isrelative"></a> ATLPath::IsRelative
 This function is an overloaded wrapper for [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660).  
  
### Syntax  
  
```  
inline BOOL IsRelative(const char* pszPath);  
inline BOOL IsRelative(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsRelative](http://msdn.microsoft.com/library/windows/desktop/bb773660) for details.  
  
 
  

## <a name="isroot"></a> ATLPath::IsRoot
 This function is an overloaded wrapper for [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674).  
  
### Syntax  
  
```  
inline BOOL IsRoot(const char* pszPath);  
inline BOOL IsRoot(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsRoot](http://msdn.microsoft.com/library/windows/desktop/bb773674) for details.  
  
 
  

## <a name="issameroot"></a> ATLPath::IsSameRoot
 This function is an overloaded wrapper for [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687).  
  
### Syntax  
  
```  
inline BOOL IsSameRoot(const char* pszPath1, const char* pszPath2);  
inline BOOL IsSameRoot(const wchar_t* pszPath1, const wchar_t* pszPath2);  
```  
  
### Remarks  
 See [PathIsSameRoot](http://msdn.microsoft.com/library/windows/desktop/bb773687) for details.  
  
 
  

## <a name="isunc"></a> ATLPath::IsUNC
 This function is an overloaded wrapper for [PathIsUNC](http://msdn.microsoft.com/library/windows/desktop/bb773712).  
  
### Syntax  
  
```  
inline BOOL IsUNC(const char* pszPath);  
inline BOOL IsUNC(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsUNC](http://msdn.microsoft.com/library/windows/desktop/bb773712) for details.  
  
 
  

## <a name="isuncserver"></a> ATLPath::IsUNCServer
 This function is an overloaded wrapper for [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722).  
  
### Syntax  
  
```  
inline BOOL IsUNCServer(const char* pszPath);  
inline BOOL IsUNCServer(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722) for details.  
  
 
  

## <a name="isuncservershare"></a> ATLPath::IsUNCServerShare
 This function is an overloaded wrapper for [PathIsUNCServerShare](http://msdn.microsoft.com/library/windows/desktop/bb773723).  
  
### Syntax  
  
```  
inline BOOL IsUNCServerShare(const char* pszPath);  
inline BOOL IsUNCServerShare(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathIsUNCServerShare](http://msdn.microsoft.com/library/windows/desktop/bb773723) for details.  
  
 
  

## <a name="makepretty"></a> ATLPath::MakePretty
 This function is an overloaded wrapper for [PathMakePretty](http://msdn.microsoft.com/library/windows/desktop/bb773725).  
  
### Syntax  
  
```  
inline BOOL MakePretty(char* pszPath);  
inline BOOL MakePretty(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathMakePretty](http://msdn.microsoft.com/library/windows/desktop/bb773725) for details.  
  
 
  

## <a name="matchspec"></a> ATLPath::MatchSpec  
 This function is an overloaded wrapper for [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727).  
  
### Syntax  
  
```  
inline BOOL MatchSpec(const char* pszPath, const char* pszSpec);  
inline BOOL MatchSpec(const wchar_t* pszPath, const wchar_t* pszSpec);  
```  
  
### Remarks  
 See [PathMatchSpec](http://msdn.microsoft.com/library/windows/desktop/bb773727) for details.  
  
 
  

## <a name="quotespaces"></a> ATLPath::QuoteSpaces  
 This function is an overloaded wrapper for [PathQuoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773739).  
  
### Syntax  
  
```  
inline void QuoteSpaces(char* pszPath);  
inline void QuoteSpaces(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathQuoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773739) for details.  
  
 
  

## <a name="relativepathto"></a> ATLPath::RelativePathTo
 This function is an overloaded wrapper for [PathRelativePathTo](http://msdn.microsoft.com/library/windows/desktop/bb773740).  
  
### Syntax  
  
```  
inline BOOL RelativePathTo(  
   char* pszPath,  
   const char* pszFrom,  
   DWORD dwAttrFrom,  
   const char* pszTo,  
   DWORD dwAttrTo);  

inline BOOL RelativePathTo(  
   wchar_t* pszPath,  
   const wchar_t* pszFrom,  
   DWORD dwAttrFrom,  
   const wchar_t* pszTo,  
   DWORD dwAttrTo);  
```  
  
### Remarks  
 See [PathRelativePathTo](http://msdn.microsoft.com/library/windows/desktop/bb773740) for details.  
  
 
  

## <a name="removeargs"></a> ATLPath::RemoveArgs  
 This function is an overloaded wrapper for [PathRemoveArgs](http://msdn.microsoft.com/library/windows/desktop/bb773742).  
  
### Syntax  
  
```  
inline void RemoveArgs(char* pszPath);  
inline void RemoveArgs(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathRemoveArgs](http://msdn.microsoft.com/library/windows/desktop/bb773742) for details.  
  
 
  

## <a name="removebackslash"></a> ATLPath::RemoveBackslash
 This function is an overloaded wrapper for [PathRemoveBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773743).  
  
### Syntax  
  
```  
inline char* RemoveBackslash(char* pszPath);  
inline wchar_t* RemoveBackslash(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathRemoveBackslash](http://msdn.microsoft.com/library/windows/desktop/bb773743) for details.  
  
 
  

## <a name="removeblanks"></a> ATLPath::RemoveBlanks
 This function is an overloaded wrapper for [PathRemoveBlanks](http://msdn.microsoft.com/library/windows/desktop/bb773745).  
  
### Syntax  
  
```  
inline void RemoveBlanks(char* pszPath);  
inline void RemoveBlanks(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathRemoveBlanks](http://msdn.microsoft.com/library/windows/desktop/bb773745) for details.  
  
 
  

## <a name="removeextension"></a> ATLPath::RemoveExtension
 This function is an overloaded wrapper for [PathRemoveExtension](http://msdn.microsoft.com/library/windows/desktop/bb773746).  
  
### Syntax  
  
```  
inline void RemoveExtension(char* pszPath);  
inline void RemoveExtension(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathRemoveExtension](http://msdn.microsoft.com/library/windows/desktop/bb773746) for details.  
  
 
  

## <a name="removefilespec"></a> ATLPath::RemoveFileSpec
 This function is an overloaded wrapper for [PathRemoveFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773748).  
  
### Syntax  
  
```  
inline BOOL RemoveFileSpec(char* pszPath);  
inline BOOL RemoveFileSpec(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathRemoveFileSpec](http://msdn.microsoft.com/library/windows/desktop/bb773748) for details.  
  
 
  

## <a name="renameextension"></a> ATLPath::RenameExtension
 This function is an overloaded wrapper for [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749).  
  
### Syntax  
  
```  
inline BOOL RenameExtension(char* pszPath, const char* pszExt);  
inline BOOL RenameExtension(wchar_t* pszPath, const wchar_t* pszExt);  
```  
  
### Remarks  
 See [PathRenameExtension](http://msdn.microsoft.com/library/windows/desktop/bb773749) for details.  
  
 
  

## <a name="skiproot"></a> ATLPath::SkipRoot
 This function is an overloaded wrapper for [PathSkipRoot](http://msdn.microsoft.com/library/windows/desktop/bb773754).  
  
### Syntax  
  
```  
inline char* SkipRoot(const char* pszPath);  
inline wchar_t* SkipRoot(const wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathSkipRoot](http://msdn.microsoft.com/library/windows/desktop/bb773754) for details.  
  
 
  

## <a name="strippath"></a> ATLPath::StripPath
 This function is an overloaded wrapper for [PathStripPath](http://msdn.microsoft.com/library/windows/desktop/bb773756).  
  
### Syntax  
  
```  
inline void StripPath(char* pszPath);  
inline void StripPath(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathStripPath](http://msdn.microsoft.com/library/windows/desktop/bb773756) for details.  
  
 
  


## <a name="striptoroot"></a> ATLPath::StripToRoot
 This function is an overloaded wrapper for [PathStripToRoot](http://msdn.microsoft.com/library/windows/desktop/bb773757).  
  
### Syntax  
  
```  
inline BOOL StripToRoot(char* pszPath);  
inline BOOL StripToRoot(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathStripToRoot](http://msdn.microsoft.com/library/windows/desktop/bb773757) for details.  
  
 
  

## <a name="unquotespaces"></a> ATLPath::UnquoteSpaces
 This function is an overloaded wrapper for [PathUnquoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773763).  
  
### Syntax  
  
```  
inline void UnquoteSpaces(char* pszPath);  
inline void UnquoteSpaces(wchar_t* pszPath);  
```  
  
### Remarks  
 See [PathUnquoteSpaces](http://msdn.microsoft.com/library/windows/desktop/bb773763) for details.  
  
 
  
 
