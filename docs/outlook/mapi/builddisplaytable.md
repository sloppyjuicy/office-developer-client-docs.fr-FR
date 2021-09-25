---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c49d7176b74d2d6fafd3da0a4d658dd72c7b54c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621156"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un tableau d’affichage à partir des données de page de propriétés contenues dans une ou plusieurs structures [DTPAGE.](dtpage.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpMalloc_
  
> Inutilisé ; doit être définie sur NULL. 
    
 _hInstance_
  
> [in] Instance d’un objet MAPI à partir duquel **BuildDisplayTable** récupère des ressources. 
    
 _cPages_
  
> [in] Nombre de structures [DTPAGE](dtpage.md) dans le tableau pointées par _le paramètre lpPage._ 
    
 _lpPage_
  
> [in] Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages du tableau d’affichage à construire. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau d’affichage, qui expose l’interface [IMAPITable.](imapitableiunknown.md) 
    
 _lppTblData_
  
> [in, out] Pointeur vers un pointeur vers un objet de données de table exposant [l’interface ITableData](itabledataiunknown.md) sur la table renvoyée dans _le paramètre lppTable._ Si aucun objet de données de table n’est souhaité,  _lppTblData_ doit être définie sur NULL au lieu d’une valeur de pointeur. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun
  
## <a name="remarks"></a>Remarques

MAPI utilise les fonctions pointées par  _lpAllocateBuffer_,  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart de l’allocation et de la déallocation de mémoire, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Tout ce qui est possible est lu à partir de la ressource de boîte de dialogue, notamment :
  
- Titre de la page, le membre  _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) lu à partir du titre de la boîte de dialogue dans la ressource. 
    
- Tous les titres de contrôle, c’est-à-dire, les membres  _ulbLpszLabel_ des autres structures de contrôle lisent le texte du contrôle dans la ressource. 
    
 **BuildDisplayTable** overwres anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles. Les appelants qui doivent le faire peuvent avoir **BuildDisplayTable** renvoyer l’objet de données de table  _dans lppTableData_ et y modifier des lignes ; ou ils peuvent créer la table d’affichage à la place dans un objet de données de table. 
  
Si  _lppTableData_ n’est pas définie sur NULL, le fournisseur est chargé de libérer l’objet de données de table lorsqu’il est terminé avec le tableau d’affichage. 
  

