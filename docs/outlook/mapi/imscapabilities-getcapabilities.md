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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317436"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur ce qu'une banque peut prendre en charge en fonction du sélecteur spécifié.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Paramètres

 *mscapSelector* 
  
> dans Sélecteur indiquant les fonctionnalités à renvoyer.
    
## <a name="return-value"></a>Valeur renvoyée

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Prise en charge des page d'accueil de dossier dans une banque non définie par défaut. Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Si une restriction contient des arguments non valides, tels que des propriétés non valides, la Banque ignore les arguments non valides et traite uniquement les arguments valides. Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans *mscapSelector* . 
    
VALEURS
  
> La Banque ne prend en charge aucune fonctionnalité basée sur le sélecteur donné.
    

