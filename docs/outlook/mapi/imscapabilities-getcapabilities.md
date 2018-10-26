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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583273"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur qu’une banque peut prendre en charge en fonction de la sélection spécifiée.
  
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
  
> Prise en charge pour les pages d’accueil de dossier dans une banque par défaut. Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Si une restriction contient un argument non valide tel que les propriétés non valides, la banque d’informations ignore les arguments non valides et traite uniquement les arguments valides. Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans *mscapSelector* . 
    
NULL
  
> Le magasin ne gère pas de fonction basée sur le sélecteur de donnée.
    

