---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Représente l'ID d'entrée de la Banque de remise par défaut pour le compte.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327670"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Représente l'ID d'entrée de la Banque de remise par défaut pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0018  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Balise de propriété:  <br/> |0x00180102  <br/> |
|Access  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenir ou définir cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivement.
  
L'un des effets secondaires de la définition d'une banque comme banque de remise par défaut pour un compte est que lors du démarrage d'Outlook, Outlook crée des dossiers de recherche pour ce magasin s'ils n'existent pas déjà, et répertorie le magasin dans la barre des tâches.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

