---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Représente une structure ACCT_BIN qui contient l’UID d’un compte Exchange client.
ms.openlocfilehash: 37718121de2aa8937dd9f1b78244d8da6fc0b662
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631138"
---
# <a name="prop_mapi_emsmdb_uid"></a>PROP_MAPI_EMSMDB_UID

Représente une structure [ACCT_BIN](acct_bin.md) qui contient l’UID d’un compte Exchange client. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2009  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20090102  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Utilisez [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) pour vérifier si le compte est un compte Exchange client. Si c’est le cas, **prop \_ MAPI_EMSMDB_UID** est un **ACCT_BIN** qui contient **emsmdbUID**, qui est l’ID unique, pour le compte Exchange. Si le compte n’est Exchange, cette propriété n’est pas définie.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Utilisation de comptes Exchange multiples](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Propri�t� canonique PidTagExchangeProfileSectionId](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

