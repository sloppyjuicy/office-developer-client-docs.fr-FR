---
title: Verbes de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bdad3d3f1bf09e46cf82db00f5201ee5c928e29d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587971"
---
# <a name="form-verbs"></a>Verbes de formulaires

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’interface utilisateur d’un formulaire propose généralement des éléments de menu ou des contrôles qui permettent aux utilisateurs d’agir sur le formulaire. Le rôle du serveur de formulaires est de gérer ces actions utilisateur. Cette interface est implémentée à l’aide des API Win32 standard ; L’écriture d’une interface est tout comme l’écriture d’autres interfaces pour des programmes Win32 ordinaires.
  
Souvent, les actions de l’utilisateur sont associées à des verbes. Un verbe est le nom d’une action spécifique à une classe de message spécifique. Par exemple, **Reply** est un verbe implémenté par de nombreux serveurs de formulaires, chacun d’eux peut avoir une interprétation différente de ce verbe. Les verbes sont parfois appelés commandes. 
  
> [!NOTE]
> Certains éléments de menu et contrôles d’un formulaire ne correspondent pas à un verbe. Par exemple, un **bouton Annuler** ne correspond pas à un verbe Cancel dans le serveur de formulaires. En règle générale, les verbes sont associés à des actions spécifiques à une classe de message particulière ou à un ensemble de classes de message. Bien que différentes classes de messages peuvent prendre en charge différents ensembles de verbes, toutes la prise en charge au moins le verbe Ouvrir, qui affiche l’interface utilisateur du formulaire et le charge avec les valeurs de propriété du message. 
  
Les verbes ne prennent aucun paramètre. Les formulaires qui exportent des commandes avec des paramètres variables doivent utiliser les mécanismes Automation.
  
Les clients peuvent déterminer les verbes pris en charge par une classe de message particulière via la méthode [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) qui est implémentée par le gestionnaire de formulaire MAPI. Le gestionnaire de formulaire obtient ces informations à partir du fichier de configuration du formulaire. Le verbe renvoyé par cette méthode est utilisé par le client pour afficher à l’utilisateur les commandes qui peuvent être exécutées sur un message. Par exemple, un client peut permettre aux utilisateurs de cliquer sur le bouton droit de la souris sur un message pour afficher les verbes applicables à ce message. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

