---
title: Objets de formulaire personnalisé MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 96266b948d80b07d7aefefbf29225d2f85089094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566697"
---
# <a name="mapi-custom-form-objects"></a>Objets de formulaire personnalisé MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Objets des formulaires personnalisés sont implémentées par trois composants différents :
  
- Serveur d’un formulaire.
    
- Un fournisseur de bibliothèque de formulaires.
    
- Une visionneuse de formulaire.
    
Un serveur de formulaire est des fonctionnalités similaires à une application d’objet de document composé OLE. Il s’agit d’un composant exécutable qui implémente le formulaire ; elle contrôle son affichage et les opérations qu’un utilisateur peut effectuer. MAPI démarre un serveur de formulaire à la demande lorsqu’un utilisateur souhaite afficher un message avec une classe de message qui s’affiche à l’aide d’un formulaire pris en charge par le serveur de formulaire. Serveurs de formulaire implémentent trois objets : un objet de fabrique de formulaire qui ressemble à la norme OLE fabrique de classe, un formulaire de notification récepteur pour la gestion des événements spécifiques aux formulaires et le formulaire proprement dit. 
  
Un fournisseur de bibliothèque formulaire fournit l’accès pour les clients à l’objet qui lie les messages d’une classe spécifique sur le serveur qui peut ouvrir le formulaire de cette classe pour le jeu de propriétés d’un formulaire et à son conteneur. Trois objets implémentés par les fournisseurs de bibliothèque de formulaire : un objet d’informations de formulaire, un conteneur de formulaire et un gestionnaire de formulaire permettant de lier un message sur le serveur de formulaire adéquat en fonction de classe du message.
  
Une visionneuse de formulaire est un composant qui est inclus dans les clients qui prennent en charge l’affichage des formulaires personnalisés dans les visionneuses de leur dossier. Visionneuses de formulaire ne sont pas composants MAPI indépendants, tout comme les fournisseurs de bibliothèques de formulaires et serveurs du formulaire. Visionneuses de formulaire démarrer les serveurs de formulaire et fournissent un contexte pour eux. Visionneuses de formulaire implémentent trois objets : un site de message, un contexte de vue et un récepteur de notifications pour gérer des événements spécifiques à la vue.
  
Le tableau suivant décrit tous les objets de formulaire personnalisé. 
  
|**Objet de formulaire**|**Description**|
|:-----|:-----|
|Formulaire  <br/> |Contrôle l’affichage et l’utilisation d’un formulaire personnalisé pour l’affichage des messages d’une classe spécifique.  <br/> |
|Formulaire de notification récepteur  <br/> |Gère les notifications à partir de la visionneuse de formulaire.  <br/> |
|Fabrique de formulaire  <br/> |Crée une instance d’un formulaire et permet son serveur peut rester en mémoire.  <br/> |
|Conteneur de formulaire  <br/> |Contient des informations d’un formulaire.  <br/> |
|Informations d’un formulaire  <br/> |Contient des messages et autres conteneurs de message.  <br/> |
|Gestionnaire de formulaire  <br/> |Fournit l’accès à une vue intégrée des informations d’un formulaire personnalisé qui sont liées à tous les formulaires installés. Également établit une correspondance avec les classes de message avec les identificateurs de classe de formulaire correspondant.  <br/> |
|Site de message  <br/> |Gère la manipulation des objets de formulaire à partir d’à l’intérieur du client et permet d’accéder à un objet de gestionnaire de formulaire.  <br/> |
|Contexte de vue  <br/> |Prend en charge les commandes pour activer les messages suivants et précédents et pour l’enregistrement ou l’impression du formulaire.  <br/> |
|Affichage de récepteur de notification  <br/> |Gère les notifications à partir du serveur du formulaire.  <br/> |
   
L’illustration suivante montre la relation entre les composants de formulaire personnalisé, les objets et interfaces qu’ils implémentent et les composants qui sont des utilisateurs des objets. Notez que, contrairement à la plupart des autres objets MAPI, l’objet form implémente deux interfaces qui ne sont pas liées par héritage direct. Lorsqu’un objet expose plusieurs interfaces indépendantes, un utilisateur de l’objet qui est un pointeur vers une des interfaces peut récupérer un pointeur vers une des autres interfaces. Cette possibilité de naviguer entre les implémentations d’interface d’un objet est une fonctionnalité de la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Composants de formulaire personnalisé**
  
![Composants de formulaire personnalisé] (media/amapi_67.gif "Composants de formulaire personnalisé")
  
## <a name="see-also"></a>Voir aussi

- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

