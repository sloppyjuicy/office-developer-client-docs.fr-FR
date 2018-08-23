---
title: Vue d’ensemble de la fonctionnalité MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 034f3dd8bc68462348bc92a8acf2904ab66fc798
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575608"
---
# <a name="mapi-feature-overview"></a>Vue d’ensemble de la fonctionnalité MAPI
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI intègre plusieurs fonctionnalités clées qui lui permettent de façon cohérente pour les développeurs à travailler avec et utiliser différents systèmes de messagerie de façon transparente. Ces fonctionnalités incluent une gamme complète et ouvrir l’interface de programmation et prise en charge des normes du secteur. 
  
MAPI étant une interface de programmation open, il fournit des services de manière générique, permettant aux utilisateurs d’ajouter toute personnalisation nécessaire maintenant et à l’avenir. L’interface de programmation MAPI répond aux exigences d’applications clientes avec différents besoins de messagerie, par exemple une application de traitement de texte qui ne requiert que la possibilité d’envoyer des documents ou une application de groupe de travail qui requiert la possibilité de partager et stocker différents types de données. En fait, n’importe quelle application qui doit stocker les informations dans un format particulier soit exchange peut bénéficier de l’interface de programmation MAPI. Tout fournisseur de services peut utiliser l’interface pour exposer les fonctionnalités uniques de son système de messagerie, sélectionnez les fonctionnalités qui fournissent le meilleur parti aux utilisateurs de l’application.
  
MAPI fournit une séparation entre l’interface de programmation utilisée par les applications clientes de messagerie frontal et l’interface de programmation utilisée par les fournisseurs de services de serveur principal. Séparation de l’interface de client à partir du fournisseur de service permet à une seule application à utiliser plusieurs systèmes de messagerie et plusieurs applications d’utiliser un fournisseur de service unique. Chaque composant fonctionne avec une interface d’utilisateur Windows Microsoft courants. Il s’agit d’un grand intérêt pour les utilisateurs. Les utilisateurs peuvent sélectionner à partir d’une variété de systèmes, en fonction de leurs besoins à tout moment et peuvent fonctionner avec chaque système sélectionné, offrant ainsi indépendance true à partir de systèmes de messagerie spécifiques. 
  
Par exemple, une seule application client de messagerie peut recevoir des messages à partir d’un flux RSS, la messagerie vocale et télécopie. Messages provenant de tous ces systèmes peuvent être placées dans un seul emplacement, ou universel boîte de réception, à l’arrivée. Avoir une seule application gérer tous ces systèmes réduit le coût de développement, de formation des utilisateurs et de l’administration système. 
  
Séparation de l’interface de client à partir de l’interface de fournisseur supprime les dépendances de programmation de l’application par le système de messagerie et vice versa. Les développeurs d’applications clientes et des fournisseurs de services écrivent du code pour un ensemble de fonctionnalités MAPI standard, plutôt que d’un ensemble divers de spécifiques à l’application ou messages fonctionnalités spécifiques au système. Les développeurs se concentrer uniquement sur leur composant, s’il est un client ou fournisseur de services MAPI gère le reste, réduire les coûts et les temps de développement.
  
L’interface de programmation MAPI fournit un ensemble complet de fonctionnalités. MAPI vise au nouveau marché puissant d’applications de groupe de travail : applications qui communiquent avec ces différents systèmes de messagerie en tant que télécopie, déc All-In-1, la messagerie vocale, des services de communications publics tels que AT & T Easylink, CompuServe et Services MCI MESSAGERIE. L’interface MAPI permet de fournisseurs de services doivent être rendues disponibles pour tous ces systèmes. 
  
Objets compatible MAPI sont similaires dans un formulaire à des objets composant COM (Object Model). Objets COM implémentent un ensemble de méthodes qui appartiennent à une ou plusieurs des interfaces ou des collections de fonctions connexes qui définissent comment les objets se comportent et leur fonctionnement dans COM. Les utilisateurs accéder aux objets COM uniquement par le biais des pointeurs vers ces interfaces.
  
MAPI prend en charge de plusieurs plates-formes par le biais des normes du secteur comme SMTP et X.400. Vous pouvez exécuter les applications MAPI sur Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 et Windows XP. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

