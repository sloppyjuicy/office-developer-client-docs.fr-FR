---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Représente l’identificateur d’entrée de la banque de remise par défaut pour le compte.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782802"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Représente l’identificateur d’entrée de la banque de remise par défaut pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0018  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00180102  <br/> |
|Access :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenir ou définir cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.
  
Un des effets secondaires de la configuration d’un magasin en tant que la banque de remise par défaut d’un compte est que lors du démarrage d’Outlook, Outlook crée les dossiers de recherche de ce magasin si elles n’existe pas déjà et la banque dans la barre des tâches de la liste.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

