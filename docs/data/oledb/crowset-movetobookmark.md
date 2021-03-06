---
title: "CRowset::MoveToBookmark | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["ATL::CRowset::MoveToBookmark", "ATL::CRowset<TAccessor>::MoveToBookmark", "ATL.CRowset.MoveToBookmark", "ATL.CRowset<TAccessor>.MoveToBookmark", "MoveToBookmark", "CRowset::MoveToBookmark", "CRowset.MoveToBookmark", "CRowset<TAccessor>::MoveToBookmark"]
dev_langs: ["C++"]
helpviewer_keywords: ["MoveToBookmark method"]
ms.assetid: 90124723-8daf-4692-ae2f-0db26b5db920
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# CRowset::MoveToBookmark
Fetches the row marked by a bookmark or the row at a specified offset (`lSkip`) from that bookmark.  
  
## Syntax  
  
```cpp
HRESULT MoveToBookmark(const CBookmarkBase& bookmark,   
   LONG lSkip = 0) throw();  
```  
  
#### Parameters  
 `bookmark`  
 [in] A bookmark marking the location from which you want to fetch data.  
  
 `lSkip`  
 [in] The number count of rows from the bookmark to the target row. If `lSkip` is zero, the first row fetched is the bookmarked row. If `lSkip` is 1, the first row fetched is the row after the bookmarked row. If `lSkip` is -1, the first row fetched is the row before the bookmarked row.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method requires the optional interface `IRowsetLocate`, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetLocate** to `VARIANT_TRUE` and set **DBPROP_CANFETCHBACKWARDS** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
 For information about using bookmarks in consumers, see [Using Bookmarks](../../data/oledb/using-bookmarks.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../../data/oledb/crowset-class.md)   
 [CRowset::MoveNext](../../data/oledb/crowset-movenext.md)   
 [CRowset::MoveFirst](../../data/oledb/crowset-movefirst.md)   
 [IRowsetLocate::GetRowsAt](https://msdn.microsoft.com/en-us/library/ms723031.aspx)   
 [CRowset::MovePrev](../../data/oledb/crowset-moveprev.md)   
 [CRowset::MoveLast](../../data/oledb/crowset-movelast.md)