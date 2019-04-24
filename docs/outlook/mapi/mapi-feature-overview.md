---
title: Vue d'ensemble des fonctionnalités MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b1087f5156ad79b20eb31ef55c0388ffd82e1601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357714"
---
# <a name="mapi-feature-overview"></a>Vue d'ensemble des fonctionnalités MAPI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI dispose de plusieurs fonctionnalités clés qui lui permettent de fournir un moyen cohérent aux développeurs de travailler avec différents systèmes de messagerie et de les utiliser de manière transparente. Ces fonctionnalités incluent une interface de programmation complète et ouverte, et prennent en charge les normes industrielles. 
  
Dans la mesure où MAPI est une interface de programmation ouverte, il fournit des services de manière générique, ce qui permet aux utilisateurs d'ajouter les personnalisations nécessaires maintenant et à l'avenir. L'interface de programmation MAPI répond aux exigences des applications clientes avec divers besoins en matière de messagerie, tels qu'une application de traitement de texte qui n'a besoin que de la possibilité d'envoyer des documents ou une application de groupe de travail qui a besoin de partager et Stockez différents types de données. En fait, toutes les applications qui ont besoin d'échanger ou de stocker des informations dans un format particulier peuvent tirer parti de l'interface de programmation MAPI. Tout fournisseur de services peut utiliser l'interface pour exposer les fonctionnalités uniques de son système de messagerie, en sélectionnant ces fonctionnalités qui offrent le plus d'avantages aux utilisateurs des applications.
  
MAPI fournit une séparation entre l'interface de programmation utilisée par les applications clientes de messagerie frontale et l'interface de programmation utilisée par les fournisseurs de services principaux. La séparation de l'interface client du fournisseur de services permet à une seule application d'utiliser plusieurs systèmes de messagerie et plusieurs applications pour utiliser un seul fournisseur de services. Chaque composant fonctionne avec une interface utilisateur Microsoft Windows commune. Il s'agit d'un avantage précieux pour les utilisateurs. Les utilisateurs peuvent choisir parmi un large éventail de systèmes, en fonction de leurs besoins à tout moment, et peuvent travailler de manière cohérente avec chaque système sélectionné, ce qui garantit une véritable indépendance par rapport à des systèmes de messagerie spécifiques. 
  
Par exemple, une application cliente de messagerie unique peut recevoir des messages à partir d'une télécopie, d'une messagerie vocale et d'un flux RSS. Les messages de tous ces systèmes peuvent être placés dans un seul emplacement, ou boîte de réception universelle, à l'arrivée. Le fait d'avoir une seule application à gérer tous ces systèmes réduit le coût du développement, de la formation des utilisateurs et de l'administration du système. 
  
La séparation de l'interface client de l'interface du fournisseur supprime toutes les dépendances de programmation de l'application par le système de messagerie et vice versa. Les développeurs d'applications clientes et de fournisseurs de services écrivent du code dans un ensemble standard de fonctionnalités MAPI, au lieu d'un ensemble varié de fonctionnalités propres aux applications ou au système de messagerie. Les développeurs se concentrent uniquement sur leur composant, qu'il s'agisse d'un client ou d'un fournisseur de services, et MAPI gère le reste, ce qui réduit le temps et les coûts de développement.
  
L'interface de programmation MAPI fournit un ensemble complet de fonctionnalités. MAPI est destiné au nouveau marché puissant des applications de groupe de travail (applications qui communiquent avec ces différents systèmes de messagerie en tant que services de télécopie, DEC All-in-1, messagerie vocale et services de communication publics, tels que les services AT&T Easylinks, CompuServe et MCI) E-mails. L'interface MAPI permet aux fournisseurs de services d'être mis à disposition pour tous ces systèmes. 
  
Les objets conformes à la norme MAPI sont semblables sous la forme d'objets COM (Component Object Model). Les objets COM implémentent un ensemble de méthodes qui appartiennent à une ou plusieurs interfaces, ou des collections de fonctions associées qui définissent la façon dont les objets se comportent et fonctionnent dans COM. Les utilisateurs accèdent à des objets COM uniquement par le biais de pointeurs vers ces interfaces.
  
MAPI offre une prise en charge multiplateforme grâce à des normes industrielles telles que SMTP et X. 400. Vous pouvez exécuter des applications MAPI sur Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 et Windows XP. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

