---
title: Objets de formulaires personnalisés MAPI
description: Décrit comment les objets pour les formulaires personnalisés sont implémentés par trois composants différents ; serveur de formulaires, fournisseur de bibliothèque de formulaires et visionneuse de formulaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
ms.openlocfilehash: 877b2ed6bcbb9174794734f842ef02f12eea1786
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816282"
---
# <a name="mapi-custom-form-objects"></a>Objets de formulaires personnalisés MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets pour les formulaires personnalisés sont implémentés par trois composants différents :
  
- Serveur de formulaires.
    
- Fournisseur de bibliothèque de formulaires.
    
- Visionneuse de formulaires.
    
Les fonctionnalités d’un serveur de formulaires sont similaires à celles d’une application objet de document composé OLE. Il s’agit d’un composant exécutable qui implémente le formulaire ; il contrôle son affichage et les opérations qu’un utilisateur peut effectuer. MAPI démarre un serveur de formulaires à la demande lorsqu’un utilisateur souhaite afficher un message avec une classe de message affichée à l’aide d’un formulaire pris en charge par le serveur de formulaires. Les serveurs de formulaires implémentent trois objets : un objet de fabrique de formulaires qui ressemble à la fabrique de classes OLE standard, un récepteur de conseils de formulaire pour la gestion des événements spécifiques au formulaire et le formulaire lui-même. 
  
Un fournisseur de bibliothèque de formulaires fournit aux clients l’accès à l’ensemble de propriétés d’un formulaire, à son conteneur et à l’objet qui lie les messages d’une classe spécifique au serveur qui peut ouvrir le formulaire pour cette classe. Les fournisseurs de bibliothèque de formulaires implémentent trois objets : un objet d’informations de formulaire, un conteneur de formulaires et un gestionnaire de formulaires pour lier un message au serveur de formulaires approprié en fonction de la classe du message.
  
Une visionneuse de formulaires est un composant inclus dans les clients qui prennent en charge l’affichage de formulaires personnalisés dans leurs visionneuses de dossiers. Les visionneuses de formulaires ne sont pas des composants MAPI indépendants, tout comme les fournisseurs de bibliothèques de formulaires et les serveurs de formulaires. Les visionneuses de formulaires démarrent les serveurs de formulaires et fournissent un contexte pour eux. Les visionneuses de formulaire implémentent trois objets : un site de message, un contexte d’affichage et un récepteur de conseils pour la gestion des événements spécifiques à la vue.
  
Le tableau suivant décrit tous les objets de formulaire personnalisés. 
  
|**Form (objet)**|**Description**|
|:-----|:-----|
|Formulaire  <br/> |Contrôle l’affichage et le fonctionnement d’un formulaire personnalisé pour afficher les messages d’une classe spécifique. |
|Récepteur d’avis de formulaire  <br/> |Gère les notifications de la visionneuse de formulaires. |
|Fabrique de formulaires  <br/> |Crée une instance d’un formulaire et permet à son serveur de rester en mémoire. |
|Conteneur de formulaires  <br/> |Contient des informations sur le formulaire. |
|Informations sur le formulaire  <br/> |Contient des messages et d’autres conteneurs de messages. |
|Gestionnaire des formulaires  <br/> |Fournit l’accès à une vue intégrée des informations de formulaire personnalisées liées à tous les formulaires installés. Correspond également aux classes de message avec les identificateurs de classe de formulaire correspondants. |
|Site de message  <br/> |Gère la manipulation d’objets de formulaire à partir de l’intérieur du client et fournit l’accès à un objet gestionnaire de formulaires. |
|Contexte d’affichage  <br/> |Prend en charge les commandes de formulaire pour l’activation des messages suivants et précédents, ainsi que pour l’enregistrement ou l’impression. |
|Afficher le récepteur de conseils  <br/> |Gère les notifications à partir du serveur de formulaires. |
   
L’illustration suivante montre la relation entre les composants de formulaire personnalisés, les objets et les interfaces qu’ils implémentent, ainsi que les composants qui sont utilisateurs des objets. Notez que, contrairement à la plupart des autres objets MAPI, l’objet de formulaire implémente deux interfaces qui ne sont pas liées par l’héritage direct. Lorsqu’un objet expose plusieurs interfaces indépendantes, un utilisateur de l’objet qui a un pointeur vers l’une des interfaces peut récupérer un pointeur vers l’une des autres interfaces. Cette possibilité de naviguer entre les implémentations d’interface d’un objet est une fonctionnalité de la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Composants de formulaire personnalisé**
  
![Composants de formulaire personnalisé](media/amapi_67.gif "Composants de formulaire personnalisé")
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’objet et de l’interface MAPI](mapi-object-and-interface-overview.md)

