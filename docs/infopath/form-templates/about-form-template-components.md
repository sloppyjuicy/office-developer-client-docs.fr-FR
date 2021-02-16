---
title: À propos des composants de modèle de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Les modèles de formulaire Microsoft InfoPath se composent de plusieurs fichiers et composants associés pour fournir des fonctionnalités spécifiques en cas de scénario d'utilisateur final particulier ou de besoin métier. Les formulaires InfoPath sont de complexité diverse, selon le type de besoin auquel ils sont associés.
ms.openlocfilehash: 3c5adc7ec1e24af481dff7f4a8d009b2dcb6ba8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419057"
---
# <a name="about-form-template-components"></a>À propos des composants de modèle de formulaire

Les modèles de formulaire Microsoft InfoPath se composent de plusieurs fichiers et composants associés pour fournir des fonctionnalités spécifiques en cas de scénario d'utilisateur final particulier ou de besoin métier. Les formulaires InfoPath sont de complexité diverse, selon le type de besoin auquel ils sont associés.
  
Un modèle de formulaire InfoPath est avant tout un type d'application qui crée une classe spécifiée de documents XML, définit leur comportement de modification et disposition, renforce la cohérence de leurs données et fournit les informations de routage qui indiquent où les stocker.
  
Il est important de savoir que les modèles de formulaire InfoPath sont composés de plusieurs fichiers différents de nombreux types variés ; ces fichiers sont collectivement appelés fichiers de formulaire. En général, un modèle de formulaire InfoPath se compose des types de fichier ci-après.
  
|**Name**|**Extension**|**Description**|
|:-----|:-----|:-----|
|Définition de formulaire  <br/> |.xsf  <br/> |Fichier généré par InfoPath contenant des informations sur tous les autres fichiers et composants utilisés dans un formulaire. Ce fichier sert de manifeste au formulaire.  <br/> |
|Schéma XML  <br/> |.xsd  <br/> |Fichiers de schéma XML utilisés pour limiter et valider les fichiers de document XML sous-jacents d'un formulaire.  <br/> |
|Vue  <br/> |.xsl  <br/> |Fichiers logiques de présentation, utilisés pour présenter, afficher et transformer les données contenues dans les fichiers de document XLM sous-jacents d'un formulaire.  <br/> |
|Modèle XML  <br/> |.xml  <br/> |Fichier .xml contenant les données par défaut qui s'affichent dans une vue lorsqu'un formulaire est créé.  <br/> |
|Présentation  <br/> |.htm, .gif, .bmp, et autres formats  <br/> |Fichiers utilisés avec les fichiers d'affichage pour créer une interface utilisateur personnalisée.  <br/> |
|Logique métier  <br/> |.dll  <br/> |Code de programmation compilée utilisé pour implémenter un comportement de modification spécifique, une validation de données, des gestionnaires d'événements, un contrôle de flux de données  et d'autres logiques métier personnalisées. La logique métier InfoPath peut s'écrire dans les langages de programmation Visual Basic et C# .NET, qui sont compilés et inclus en tant que fichiers binaires.  <br/> |
|Binaire  <br/> |.dll, .exe  <br/> | Tout composant personnalisé fournissant de la logique métier supplémentaire.  <br/> |
|Modèle de formulaire  <br/> |.xsn  <br/> |Format de fichier compressé (.cab) regroupant tous les fichiers de formulaire en un fichier.  <br/> |
   

