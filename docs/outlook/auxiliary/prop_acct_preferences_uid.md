---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Récupère l’identificateur unique (UID) de la section de profil qui stocke les préférences de compte.
ms.openlocfilehash: 31c5b282cee74e7a3ee25140a886ed1686c63617
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629621"
---
# <a name="prop_acct_preferences_uid"></a>PROP_ACCT_PREFERENCES_UID

Récupère l’identificateur unique (UID) de la section de profil qui stocke les préférences de compte. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x0022  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00220102  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **PROP_ACCT_PREFERENCES_UID** dans les appels à [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) pour récupérer la section de profil qui contient les préférences de compte. 
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [À propos des paramètres anti-spam](about-anti-spam-settings.md)

