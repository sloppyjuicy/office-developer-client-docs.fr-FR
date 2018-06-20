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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784232"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**S’applique à**: Outlook 
  
Obtient des informations sur qu’une banque peut prendre en charge en fonction de la sélection spécifiée.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Paramètres

 *mscapSelector* 
  
> [in] Sélecteur indiquant les fonctionnalités à renvoyer.
    
## <a name="return-value"></a>Valeur renvoy�e

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Prise en charge pour les pages d’accueil de dossier dans une banque par défaut. Cela peut être renvoyé si **MSCAP_SEL_FOLDER** est spécifié dans *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Si une restriction contient un argument non valide tel que les propriétés non valides, la banque d’informations ignore les arguments non valides et traite uniquement les arguments valides. Cela peut être renvoyé si **MSCAP_SEL_RESTRICTION** est spécifié dans *mscapSelector* . 
    
NULL
  
> Le magasin ne gère pas de fonction basée sur le sélecteur de donnée.
    

