---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Récupère l’identificateur unique (UID) de la section profil qui stocke les préférences.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395291"
---
# <a name="propacctpreferencesuid"></a>PROP_ACCT_PREFERENCES_UID

Récupère l’identificateur unique (UID) de la section profil qui stocke les préférences. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0 x 0022  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00220102  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **PROP_ACCT_PREFERENCES_UID** dans les appels à [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) pour récupérer la section profil qui contient les préférences du compte. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [À propos des paramètres anti-spam](about-anti-spam-settings.md)

