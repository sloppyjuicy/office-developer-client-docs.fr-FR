---
title: Format des fichiers config des formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
ms.openlocfilehash: af25d21b6c3793b38b4ff535e0274b760d32191e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375488"
---
# <a name="file-format-of-form-configuration-files"></a>Format des fichiers config des formulaires

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fichier de configuration de formulaire est un fichier mis en forme créé par les développeurs de formulaires pour définir un formulaire.
  
Étant donné que les fichiers de configuration de formulaire sont utilisés par les gestionnaires de formulaires pour charger des formulaires, chaque formulaire doit être défini à l’aide d’un fichier de configuration de formulaire. Les fichiers de configuration de formulaire doivent avoir l’extension de nom de fichier .cfg. Le fichier suit la syntaxe générale d’un Windows d’initialisation (.ini fichier). 

Il est divisé en sections nommées et chaque section contient une série d’entrées et de valeurs. Les valeurs ont l’un des types suivants : chaîne, chaîne affichée, chaîne de plateforme, chemin d’accès, nombres longs ou identificateur global unique, **GUID**. Les fichiers de configuration de formulaire peuvent être créés avec n’importe quel éditeur de texte ou processeur de texte capable d’enregistrer des fichiers texte.
  

