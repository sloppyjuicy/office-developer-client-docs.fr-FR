---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: Représente l'ID d'entrée du dossier de remise par défaut pour le compte.
ms.openlocfilehash: 1bac4890791edfe661599d383e2cb048bf4c42fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327698"
---
# <a name="propacctdeliveryfolder"></a>PROP_ACCT_DELIVERY_FOLDER

Représente l'ID d'entrée du dossier de remise par défaut pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0019  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Balise de propriété:  <br/> |0x00190102  <br/> |
|Access  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenir ou définir cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivement.
  
Le dossier de remise par défaut est **boîte de réception**.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

