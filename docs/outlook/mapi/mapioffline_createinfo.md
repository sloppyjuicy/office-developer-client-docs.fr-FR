---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: La MAPIOFFLINE_CREATEINFO structure est utilisée avec HrCreateOfflineObj.
ms.openlocfilehash: c6504183fe637fb3ca48685cbc984c9e59fde598
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741839"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette structure est utilisée [avec HrCreateOfflineObj](hrcreateofflineobj.md).
  
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
  
> Taille de la structure.

 **ulCreateFlags**
  
> Elle doit être 0.

 **pwszProfileName**
  
> Nom du profil.

 **ulCapabilities**
  
> Masque de bits des indicateurs de fonctionnalité suivants.

|Valeur |Description |
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |L’objet hors connexion est capable de passer hors connexion. |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |L’objet hors connexion est capable de passer en ligne. |

 **pGUID**
  
> Pointeur vers un GUID utilisé pour identifier de manière unique ce type d’objet hors connexion à partir d’autres objets hors connexion. GUID_GlobalState fait référence à l’objet hors connexion global que les objets peuvent utiliser comme objet parent.

 **pInstance**
  
> Pointeur vers le GUID qui identifie de manière unique cet objet hors connexion. Il est utilisé pour déconnecter ces objets hors connexion des autres objets.

 **pParent**
  
> Pointeur vers l’objet hors connexion qui est le parent de cet objet hors connexion et dont cet objet hors connexion héritera des modifications.

 **pMAPISupport**
  
> Identifie l’objet de prise en charge MAPI qui utilisera cet objet hors connexion. Par exemple, si cet objet hors connexion est utilisé pour suivre l’état hors connexion et en ligne d’un magasin, il s’agit de l’objet de prise en charge des magasins. Toutefois, s’il s’agit d’un objet hors connexion pour un objet sans objet de prise en charge, il peut être NULL.

 **pAggregateInfo**
  
> Pointeur vers une structure MAPIOFFLINE_AGGREGATEINFO de base. Pour plus d’informations, [voir MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).

 **pConnectInfo**
  
> Doit être null.

## <a name="see-also"></a>Voir aussi

[HrCreateOfflineObj](hrcreateofflineobj.md)
 [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)
