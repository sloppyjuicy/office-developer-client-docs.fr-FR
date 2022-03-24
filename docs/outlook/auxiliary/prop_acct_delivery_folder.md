---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: Représente l’ID d’entrée du dossier de remise par défaut du compte.
ms.openlocfilehash: 73cd95dc3e81de991bcf5f2ff15bf1956d4fd6d9
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723928"
---
# <a name="prop_acct_delivery_folder"></a>PROP_ACCT_DELIVERY_FOLDER

Représente l’ID d’entrée du dossier de remise par défaut du compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x0019  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00190102  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez ou définissez cette propriété à l’aide [d’IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.
  
Le dossier de remise par défaut est **Boîte de réception**.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

