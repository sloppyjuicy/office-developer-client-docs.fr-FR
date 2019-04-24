---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Renvoie l'accountsendstamp.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327607"
---
# <a name="propacctsendstamp"></a>PROP_ACCT_SEND_STAMP

Renvoie le cachet «envoyer».
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x000E  <br/> |
|Type de propriété:  <br/> |PT_UNICODE  <br/> |
|Balise de propriété:  <br/> |0x000E001F  <br/> |
|Access  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

