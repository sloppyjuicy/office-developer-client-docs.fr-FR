---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577687"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une table de l’affichage de données de la propriété page contenues dans une ou plusieurs structures [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>Paramètres

 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _lpMalloc_
  
> Inutilisés ; doit être défini avec la valeur NULL. 
    
 _hInstance_
  
> [in] Une instance d’un objet MAPI à partir de laquelle **BuildDisplayTable** récupère les ressources. 
    
 _cPages_
  
> [in] Nombre de structures [DTPAGE](dtpage.md) dans le tableau indiqué par le paramètre _lpPage_ . 
    
 _lpPage_
  
> [in] Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages de tableau d’affichage à générer. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table d’affichage, qui expose l’interface [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [entrée, sortie] Pointeur vers un pointeur vers un objet de données de table exposant l’interface [ITableData](itabledataiunknown.md) sur la table renvoyée dans le paramètre _lppTable_ . Si aucun objet de données de table n’est souhaitée, _lppTblData_ doit être défini sur NULL au lieu d’une valeur de pointeur. 
    
## <a name="return-value"></a>Valeur renvoy�e

Aucune
  
## <a name="remarks"></a>Remarques

MAPI utilise les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet par exemple [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Tout possible est lu à partir de la ressource de la boîte de dialogue, y compris :
  
- Le titre de la page qui est, le membre _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) lire le titre de la boîte de dialogue de la ressource. 
    
- Tous les titres de contrôle qui est, les membres _ulbLpszLabel_ d’autres structures de contrôle lire le texte du contrôle de la ressource. 
    
 **BuildDisplayTable** remplace tout élément transmis dans les structures de contrôle d’entrée avec des informations à partir de la ressource de boîte de dialogue, ce qui signifie que l’appelant de **BuildDisplayTable** ne peut pas spécifier dynamiquement des titres de page ou un contrôle. Les appelants qui ont besoin de faire qui peuvent avoir **BuildDisplayTable** retourner l’objet de données de table _lppTableData_ et modifier des lignes ou qu’elles peuvent construire la table affichage manuellement dans un objet de données de table à la place. 
  
Si _lppTableData_ n’est pas défini sur NULL, le fournisseur est chargé de libérer l’objet de données de table lorsqu’il a terminé l’affichage de la table. 
  

