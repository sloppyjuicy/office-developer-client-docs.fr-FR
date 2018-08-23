---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ffac4328401b8afbc07eb650ea6c08da5f9c51b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594494"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette structure est utilisée avec [HrCreateOfflineObj](hrcreateofflineobj.md).
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> La taille de structure.
    
 **ulCreateFlags**
  
> Il doit être 0.
    
 **pwszProfileName**
  
> Nom du profil.
    
 **ulCapabilities**
  
> Masque de bits des indicateurs de capacité suivants.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |L’objet en mode hors connexion est capable de passer en mode hors connexion.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |L’objet en mode hors connexion est capable de passer en ligne.  <br/> |
   
 **pGUID**
  
> Pointeur vers un GUID qui sert à identifier de manière unique ce type d’objet en mode hors connexion à partir d’autres objets en mode hors connexion. GUID_GlobalState fait référence à l’objet en mode hors connexion global qui les objets peuvent utiliser en tant qu’objet parent.
    
 **pInstance**
  
> Pointeur vers un GUID qui identifie de manière unique cet objet en mode hors connexion. Il est utilisé pour clarifier cette objets en mode hors connexion à partir d’autres objets.
    
 **pParent**
  
> Pointeur vers l’objet en mode hors connexion qui est le parent de cet objet en mode hors connexion et dont les modifications hérite de cet objet en mode hors connexion.
    
 **pMAPISupport**
  
>  Identifie l’objet de prise en charge MAPI que qui utilisera cet objet en mode hors connexion. Par exemple, si cet objet en mode hors connexion est utilisé pour suivre un magasin hors connexion et l’état en ligne, puis il est les magasins de prendre en charge objet. Toutefois, s’il s’agit d’un objet en mode hors connexion pour un objet avec aucun objet de prise en charge qu’il peut être NULL. 
    
 **pAggregateInfo**
  
> Pointeur vers une structure MAPIOFFLINE_AGGREGATEINFO. Pour plus d’informations, voir [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Doit être null.
    
## <a name="see-also"></a>Voir aussi



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

