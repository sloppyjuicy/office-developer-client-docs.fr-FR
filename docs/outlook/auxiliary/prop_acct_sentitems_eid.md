---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l’identificateur d’entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782805"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Représente l’identificateur d’entrée du dossier par défaut pour les éléments envoyés pour le compte. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0 x 0020  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00200102  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Le dossier éléments envoyés par défaut est **Éléments envoyés**.
  
Cette propriété est en lecture seule pour les comptes POP3 et IMAP. Essayez de définir cette propriété pour ces types de comptes renvoie **E_ACCT_NOT_FOUND**. 
  

