---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l'ID d'entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327586"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Représente l'ID d'entrée du dossier par défaut pour les éléments envoyés pour le compte. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0020  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Balise de propriété:  <br/> |0x00200102  <br/> |
|Access  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md).
  
Le dossier par défaut pour les éléments envoyés est **éléments envoyés**.
  
Cette propriété est en lecture seule pour les comptes POP3 et IMAP. La tentative de définition de cette propriété pour ces types de comptes renvoie **E_ACCT_NOT_FOUND**. 
  

