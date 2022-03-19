---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l’ID d’entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: 1fc2380eed78286fe1e05cb51612a46e62f232bf
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627129"
---
# <a name="prop_acct_sentitems_eid"></a>PROP_ACCT_SENTITEMS_EID

Représente l’ID d’entrée du dossier par défaut pour les éléments envoyés pour le compte. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x0020  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00200102  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide d’IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Le dossier par défaut pour les éléments envoyés est **Éléments envoyés**.
  
Cette propriété est en lecture seule pour les comptes POP3 et IMAP. Si vous tentez de définir cette propriété pour ces types de comptes, **E_ACCT_NOT_FOUND.** 
  

