---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Représente une structure ACCT_BIN qui contient l’UID d’un compte Exchange.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782834"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Représente une structure [ACCT_BIN](acct_bin.md) qui contient l’UID d’un compte Exchange. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2009  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20090102  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Utilisez [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) pour vérifier si le compte est un compte Exchange. S’il s’agit, **propriétés\_MAPI_EMSMDB_UID** est un **ACCT_BIN** contenant **emsmdbUID**, qui est l’ID unique, pour le compte Exchange. Si le compte n’est pas un compte Exchange, cette propriété est non définie.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Utilisation de plusieurs comptes Exchange](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Propri�t� canonique PidTagExchangeProfileSectionId](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

