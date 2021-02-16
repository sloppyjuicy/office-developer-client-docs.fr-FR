---
title: Objets de formulaire personnalisé MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318244"
---
# <a name="mapi-custom-form-objects"></a>Objets de formulaire personnalisé MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets pour les formulaires personnalisés sont implémentés par trois composants différents :
  
- Un serveur de formulaires.
    
- Fournisseur de bibliothèque de formulaires.
    
- Visionneuse de formulaires.
    
La fonctionnalité d’un serveur de formulaires est similaire à celle d’une application d’objet document composé OLE. Il s’agit d’un composant exécutable qui implémente le formulaire ; Il contrôle son affichage et les opérations qu’un utilisateur peut effectuer. MAPI démarre un serveur de formulaires sur demande lorsqu’un utilisateur souhaite afficher un message avec une classe de message affichée à l’aide d’un formulaire pris en charge par le serveur de formulaires. Les serveurs de formulaires implémentent trois objets : un objet de fabrique de formulaires qui ressemble à la fabrique de classes OLE standard, un formulaire conseiller le sink pour la gestion des événements spécifiques au formulaire et le formulaire lui-même. 
  
Un fournisseur de bibliothèque de formulaires fournit aux clients l’accès à l’ensemble de propriétés d’un formulaire, à son conteneur et à l’objet qui lie les messages d’une classe spécifique au serveur qui peut ouvrir le formulaire pour cette classe. Les fournisseurs de bibliothèques de formulaires implémentent trois objets : un objet d’informations de formulaire, un conteneur de formulaires et un gestionnaire de formulaires pour lier un message au serveur de formulaires approprié en fonction de la classe du message.
  
Une visionneuse de formulaires est un composant inclus dans les clients qui supportent l’affichage de formulaires personnalisés dans leurs visionneuses de dossiers. Les visionneuses de formulaires ne sont pas des composants MAPI indépendants, tout comme les fournisseurs de bibliothèques de formulaires et les serveurs de formulaires. Les visionneuses de formulaire démarrent les serveurs de formulaires et leur fournissent du contexte. Les visionneuses de formulaires implémentent trois objets : un site de message, un contexte d’affichage et un sink de conseil pour la gestion des événements spécifiques à l’affichage.
  
Le tableau suivant décrit tous les objets de formulaire personnalisés. 
  
|**Form (objet)**|**Description**|
|:-----|:-----|
|Formulaire  <br/> |Contrôle l’affichage et le fonctionnement d’un formulaire personnalisé pour l’affichage des messages d’une classe spécifique.  <br/> |
|Formulaire de conseiller en cas de sink  <br/> |Gère les notifications de la visionneuse de formulaires.  <br/> |
|Fabrique de formulaires  <br/> |Crée une instance d’un formulaire et permet à son serveur de rester en mémoire.  <br/> |
|Conteneur de formulaires  <br/> |Contient des informations sur le formulaire.  <br/> |
|Informations sur le formulaire  <br/> |Contient des messages et d’autres conteneurs de messages.  <br/> |
|Gestionnaire des formulaires  <br/> |Permet d’accéder à une vue intégrée des informations de formulaire personnalisé liées à tous les formulaires installés. Fait également correspondre les classes de message avec les identificateurs de classe de formulaire correspondants.  <br/> |
|Site de message  <br/> |Gère la manipulation des objets de formulaire à partir de l’intérieur du client et donne accès à un objet gestionnaire de formulaires.  <br/> |
|Contexte d’affichage  <br/> |Prend en charge les commandes de formulaire pour l’activation des messages suivants et précédents et pour l’enregistrement ou l’impression.  <br/> |
|Afficher le dos à l’avis  <br/> |Gère les notifications à partir du serveur de formulaires.  <br/> |
   
L’illustration suivante montre la relation entre les composants de formulaire personnalisés, les objets et les interfaces qu’ils implémentent et les composants qui sont des utilisateurs des objets. Notez que, contrairement à la plupart des autres objets MAPI, l’objet de formulaire implémente deux interfaces qui ne sont pas liées par un héritage direct. Lorsqu’un objet expose plusieurs interfaces indépendantes, un utilisateur de l’objet qui possède un pointeur vers l’une des interfaces peut récupérer un pointeur vers n’importe quelle autre interface. Cette possibilité de naviguer entre les implémentations d’interface d’un objet est une fonctionnalité de la méthode [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) 
  
**Composants de formulaire personnalisé**
  
![Composants de formulaire personnalisés](media/amapi_67.gif "Composants de formulaire personnalisés")
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

