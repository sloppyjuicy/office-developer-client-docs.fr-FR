---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409257"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur ce qu’un magasin peut prendre en charge en fonction du sélecteur spécifié.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Paramètres

 *mscapSelector* 
  
> [in] Sélecteur indiquant les fonctionnalités à renvoyer.
    
## <a name="return-value"></a>Valeur renvoyée

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Prise en charge des pages d’accueil de dossiers dans un magasin autre que le magasin par défaut. Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans  *mscapSelector*  . 
    
MSCAP_RES_ANNOTATION
  
> Si une restriction contient des arguments non valides tels que des propriétés non valides, la boutique ignore les arguments non valides et traite uniquement les arguments valides. Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans  *mscapSelector*  . 
    
NULL
  
> Le magasin ne prend en charge aucune fonctionnalité basée sur le sélecteur donné.
    

