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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431595"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une table d'affichage à partir des données de la page de propriétés contenues dans une ou plusieurs structures [DTPAGE](dtpage.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpMalloc_
  
> Inutilisés doit être défini sur NULL. 
    
 _hInstance_
  
> dans Instance d'un objet MAPI à partir de laquelle **BuildDisplayTable** récupère des ressources. 
    
 _cPages_
  
> dans Nombre de structures [DTPAGE](dtpage.md) dans le tableau vers lequel pointe le paramètre _lpPage_ . 
    
 _lpPage_
  
> dans Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages de table d'affichage à créer. 
    
 _ulFlags_
  
> dans Masque de réindicateur des indicateurs. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table d'affichage, qui expose l'interface [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [in, out] Pointeur vers un pointeur vers un objet de données de tableau exposant l'interface [ITableData](itabledataiunknown.md) sur le tableau renvoyé dans le paramètre _lppTable_ . Si aucun objet de données de table n'est souhaité, _lppTblData_ doit être défini sur null au lieu d'une valeur de pointeur. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun
  
## <a name="remarks"></a>Remarques

MAPI utilise les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire, notamment pour allouer de la mémoire aux applications clientes lors de l'appel d'interfaces d'objets comme [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Tout ce qu'il est possible de lire à partir de la ressource Dialog, y compris:
  
- Le titre de la page, qui est le membre _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) , qui est lu à partir du titre de la boîte de dialogue dans la ressource. 
    
- Tous les titres de contrôle qui sont les membres _ulbLpszLabel_ d'autres structures de contrôle lues à partir du texte du contrôle de la ressource. 
    
 **BuildDisplayTable** remplace tous les éléments transmis dans les structures de contrôle d'entrée par les informations de la ressource Dialog, ce qui signifie que l'appelant de **BuildDisplayTable** ne peut pas spécifier dynamiquement des titres de page ou de contrôle. Les appelants qui doivent effectuer cette opération peuvent avoir **BuildDisplayTable** renvoyer l'objet de données de tableau dans _lppTableData_ et modifier des lignes dans celui-ci; ou ils peuvent créer la table d'affichage manuellement dans un objet de données de table. 
  
Si _lppTableData_ n'est pas défini sur null, le fournisseur est responsable de la libération de l'objet de données de table lorsqu'il est terminé avec la table d'affichage. 
  

