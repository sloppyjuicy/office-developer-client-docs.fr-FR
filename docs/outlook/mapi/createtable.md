---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332983"
---
# <a name="createtable"></a>CreateTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée des structures et un descripteur d'objet pour un objet [ITableData](itabledataiunknown.md) qui peut être utilisé pour créer le contenu du tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> dans Pointeur vers un identificateur d'interface (IID) pour l'objet de données de table. L'identificateur d'interface valide est IID_IMAPITableData. Le fait de transmettre NULL dans le paramètre _lpInterface_ entraîne également le cast de l'objet de données de tableau renvoyé dans le paramètre _lppTableData_ en interface standard pour un objet de données de tableau. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _ulTableType_
  
> dans Un type de table disponible pour une application cliente ou un fournisseur de services dans le cadre de la fonction [IMAPITable:: GetStatus](imapitable-getstatus.md) renvoie des données dans ses vues de tableau. Les valeurs possibles sont les suivantes : 
    
TBLTYPE_DYNAMIC 
  
> Le contenu de la table est dynamique et peut changer lorsque les données sous-jacentes sont modifiées. 
    
TBLTYPE_KEYSET 
  
> Les lignes du tableau sont fixes, mais les valeurs de ces lignes sont dynamiques et peuvent changer à mesure que les données sous-jacentes sont modifiées. 
    
TBLTYPE_SNAPSHOT 
  
> Le tableau est statique et le contenu ne change pas lorsque les données sous-jacentes sont modifiées. 
    
 _ulPropTagIndexColumn_
  
> dans Numéro d'index de la colonne à utiliser lors de la modification des données de la table. 
    
 _lpSPropTagArrayColumns_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés requises dans la table pour laquelle l'objet contient des données. 
    
 _lppTableData_
  
> remarquer Pointeur vers un pointeur vers l'objet de données de tableau renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les paramètres d'entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Une application cliente qui appelle **CreateTable** passe des pointeurs vers les fonctions MAPI que vous venez de nommer; un fournisseur de services transmet les pointeurs vers ces fonctions qu'il a reçues dans son appel d'initialisation ou qui a été récupéré avec un appel à la méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)

