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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5d4717dad51e7e6b90da59d285268761eec84d7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564149"
---
# <a name="createtable"></a>CreateTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée des structures et un handle d’objet pour un objet [ITableData](itabledataiunknown.md) qui peut être utilisé pour créer le contenu du tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de table. L’identificateur d’interface valide est IID_IMAPITableData. Passage de NULL dans le paramètre _lpInterface_ entraîne également l’objet de données de table retournée dans le paramètre _lppTableData_ pour effectuer un cast à l’interface standard pour un objet de données de table. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _ulTableType_
  
> [in] Type de table qui est disponible pour une application cliente ou d’un fournisseur de services dans le cadre des données de retour [IMAPITable::GetStatus](imapitable-getstatus.md) sur son point de vue table. Les valeurs possibles sont les suivantes : 
    
TBLTYPE_DYNAMIC 
  
> Contenu de la table est dynamique et peut changer en tant que les modifications de données sous-jacente. 
    
TBLTYPE_KEYSET 
  
> Les lignes dans le tableau sont fixe, mais les valeurs dans les lignes sont dynamiques et peuvent changer lorsque les modifications de données sous-jacente. 
    
TBLTYPE_SNAPSHOT 
  
> Le tableau est statique et le contenu n’est pas modifié lorsque les données sous-jacentes changent. 
    
 _ulPropTagIndexColumn_
  
> [in] Numéro d’index de la colonne à utiliser lors de la modification des données de la table. 
    
 _lpSPropTagArrayColumns_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés requises dans la table pour laquelle l’objet contient des données. 
    
 _lppTableData_
  
> [out] Pointeur vers un pointeur vers l’objet de données de table renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les paramètres d’entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ point [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), les fonctions [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Une application cliente appelant **Create table** passe pointeurs aux fonctions MAPI nommées uniquement ; un fournisseur de services transmet les pointeurs vers ces fonctions qu’il a reçu dans son appel d’initialisation ou récupérés par un appel à la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)

