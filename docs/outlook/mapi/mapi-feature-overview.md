---
title: Vue d’ensemble des fonctionnalités MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f1e4e09b6e1b200a8930ae7df7781a8e449539b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567220"
---
# <a name="mapi-feature-overview"></a>Vue d’ensemble des fonctionnalités MAPI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI propose plusieurs fonctionnalités clés qui lui permettent de fournir aux développeurs un moyen cohérent d’utiliser et d’utiliser différents systèmes de messagerie de façon transparente. Ces fonctionnalités incluent une interface de programmation complète et ouverte et la prise en charge des normes du secteur. 
  
MapI étant une interface de programmation ouverte, il fournit des services d’une manière générique, ce qui permet aux utilisateurs d’ajouter toute personnalisation nécessaire maintenant et à l’avenir. L’interface de programmation MAPI répond aux exigences des applications clientes ayant divers besoins de messagerie, telles qu’une application de traitement de texte qui nécessite uniquement la possibilité d’envoyer des documents, ou une application de groupe de travail qui nécessite la possibilité de partager et de stocker différents types de données. En fait, toute application qui doit échanger ou stocker des informations dans un format particulier peut bénéficier de l’interface de programmation MAPI. N’importe quel fournisseur de services peut utiliser l’interface pour exposer les fonctionnalités uniques de son système de messagerie, en sélectionnant celles qui offrent le plus d’avantages aux utilisateurs de l’application.
  
MAPI assure la séparation entre l’interface de programmation utilisée par les applications clientes de messagerie frontale et l’interface de programmation utilisée par les fournisseurs de services principaux. La séparation de l’interface client et du fournisseur de services permet à une application unique d’utiliser plusieurs systèmes de messagerie et plusieurs applications d’utiliser un seul fournisseur de services. Chaque composant fonctionne avec une interface utilisateur Windows Microsoft. Il s’agit d’un avantage pour les utilisateurs. Les utilisateurs peuvent choisir parmi divers systèmes, en fonction de leurs besoins à tout moment, et peuvent travailler de manière cohérente avec chaque système sélectionné, offrant ainsi une véritable indépendance vis-à-vis de systèmes de messagerie spécifiques. 
  
Par exemple, une application cliente de messagerie unique peut recevoir des messages à partir d’une télécopie, d’une messagerie vocale et d’un flux RSS. Les messages de tous ces systèmes peuvent être placés dans un emplacement unique ou dans une boîte de réception universelle à l’arrivée. Le fait de disposer d’une seule application gère tous ces systèmes réduit les coûts de développement, de formation des utilisateurs et d’administration du système. 
  
La séparation de l’interface client et de l’interface du fournisseur supprime toutes les dépendances de programmation placées sur l’application par le système de messagerie et inversement. Les développeurs d’applications clientes et de fournisseurs de services écrivent du code dans un ensemble standard de fonctionnalités MAPI, plutôt qu’un ensemble variés de fonctionnalités spécifiques à l’application ou au système de messagerie. Les développeurs se concentrent uniquement sur leur composant, qu’il s’agit d’un client ou d’un fournisseur de services, et MAPI gère le reste, réduisant ainsi le temps et les coûts de développement.
  
L’interface de programmation MAPI fournit un ensemble complet de fonctionnalités. MAPI s’adresse au nouveau marché puissant des applications de groupe de travail : applications qui communiquent avec des systèmes de messagerie aussi différents que la télécopie, DEC tout-en-1, la messagerie vocale et les services de communications publiques tels que AT&T Easylink Services, CompuServe et MCI MAIL. L’interface MAPI permet aux fournisseurs de services d’être disponibles pour tous ces systèmes. 
  
Les objets compatibles MAPI sont similaires sous la forme aux objets COM (Component Object Model). Les objets COM implémentent un ensemble de méthodes qui appartiennent à une ou plusieurs interfaces, ou des collections de fonctions associées qui définissent le comportement et le fonctionnement des objets dans COM. Les utilisateurs accèdent aux objets COM uniquement par le biais de pointeurs vers ces interfaces.
  
MAPI offre une prise en charge sur plusieurs plateformes par le biais de normes industrielles telles que SMTP et X.400. Vous pouvez exécuter des applications MAPI sur Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 et Windows XP. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

