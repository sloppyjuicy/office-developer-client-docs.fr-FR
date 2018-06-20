---
title: Formulaire verbes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783346"
---
# <a name="form-verbs"></a>Formulaire verbes

**S’applique à**: Outlook 
  
Interface utilisateur d’un formulaire offre généralement des éléments de menu ou des contrôles permettant aux utilisateurs d’effectuer un type d’action avec le formulaire. Il est le travail du serveur de formulaire pour gérer ces actions de l’utilisateur. Cette interface est implémentée à l’aide des API Win32 standard ; une écriture est tout simplement à rédiger des autres interfaces pour les programmes Win32 régulières.
  
Souvent, les actions de l’utilisateur sont associées à des verbes. Un verbe est le nom d’une action qui est spécifique à une certaine classe de message. Par exemple, la **réponse** est un verbe qui est implémenté par de nombreux serveurs de formulaire, chacun d'entre eux peut avoir une autre interprétation de ce verbe. Verbes sont parfois en tant que commandes. 
  
> [!NOTE]
> Pas tous les éléments de menu et les contrôles d’un formulaire correspondent à un verbe. Par exemple, un bouton **Annuler** ne correspond pas à un verbe Cancel sur le serveur du formulaire. En règle générale, les verbes sont associés à des actions qui sont spécifiques à une classe de message spécifique ou un ensemble de classes de message. Bien que les différentes classes de messages peuvent prendre en charge plusieurs ensembles de verbes, tous les prend en charge au moins le verbe Open, qui affiche l’interface utilisateur du formulaire et la charge de valeurs de propriété du message. 
  
Verbes ne peuvent prendre aucun paramètre. Formulaires exporter des commandes à l’aide des paramètres variables doivent utiliser les mécanismes d’Automation.
  
Les clients peuvent déterminer les verbes sont pris en charge par une classe de message spécifique par le biais de la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , qui est implémentée par le Gestionnaire de formulaire MAPI. Le Gestionnaire de formulaire obtient ces informations à partir du fichier de configuration du formulaire. Le jeu de verbe renvoyé par cette méthode est utilisé par le client pour afficher les commandes pouvant être exécutées sur un message. Par exemple, un client peut activer les utilisateurs à cliquer sur le bouton droit de la souris sur un message à afficher les verbes applicables à ce message. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

