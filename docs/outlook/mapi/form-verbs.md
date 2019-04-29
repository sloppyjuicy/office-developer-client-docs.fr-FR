---
title: Verbes de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424027"
---
# <a name="form-verbs"></a>Verbes de formulaires

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'interface utilisateur d'un formulaire propose généralement des éléments de menu ou des contrôles qui permettent aux utilisateurs de prendre des mesures avec le formulaire. Il s'agit du travail du serveur de formulaire pour gérer ces actions de l'utilisateur. Cette interface est implémentée à l'aide des API Win32 standard; l'écriture d'une est similaire à celle de l'écriture d'autres interfaces pour les programmes Win32 classiques.
  
Les actions de l'utilisateur sont souvent associées à des verbes. Un verbe est le nom d'une action spécifique à une certaine classe de message. Par exemple, la **réponse** est un verbe implémenté par de nombreux serveurs de formulaires, dont chacun peut avoir une interprétation différente de ce verbe. Les verbes sont parfois appelés commandes. 
  
> [!NOTE]
> Les éléments de menu et les contrôles d'un formulaire ne correspondent pas tous à un verbe. Par exemple, un bouton **Annuler** ne correspond pas à un verbe Cancel dans le serveur de formulaires. En règle générale, les verbes sont associés à des actions propres à une classe de message particulière ou à un ensemble de classes de message. Bien que différentes classes de messages puissent prendre en charge différents ensembles de verbes, toutes prennent en charge au moins le verbe Open, qui affiche l'interface utilisateur du formulaire et le charge avec les valeurs de propriété du message. 
  
Les verbes ne peuvent pas prendre de paramètres. Les formulaires qui exportent des commandes avec des paramètres variables doivent utiliser les mécanismes d'automatisation.
  
Les clients peuvent déterminer les verbes pris en charge par une classe de message particulière par le biais de la méthode [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) , qui est implémentée par le gestionnaire de formulaires MAPI. Le gestionnaire de formulaires obtient ces informations à partir du fichier de configuration du formulaire. Le jeu de verbes renvoyé par cette méthode est utilisé par le client pour montrer à l'utilisateur les commandes pouvant être exécutées sur un message. Par exemple, un client peut permettre aux utilisateurs de cliquer avec le bouton droit de la souris sur un message pour afficher les verbes applicables à ce message. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

