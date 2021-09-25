---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l’ID d’entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: e9073a5b113ddd1181cb46ce44ac238833893636
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614345"
---
# <a name="prop_acct_sentitems_eid"></a>PROP_ACCT_SENTITEMS_EID

Représente l’ID d’entrée du dossier par défaut pour les éléments envoyés pour le compte. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0020  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00200102  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Le dossier par défaut pour les éléments envoyés est **Éléments envoyés.**
  
Cette propriété est en lecture seule pour les comptes POP3 et IMAP. Si vous essayez de définir cette propriété pour ces types de comptes, E_ACCT_NOT_FOUND **.** 
  

