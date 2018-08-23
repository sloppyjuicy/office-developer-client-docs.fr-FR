---
title: Bibliothèques de formulaires de dossiers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580550"
---
# <a name="folder-form-libraries"></a>Bibliothèques de formulaires de dossiers

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Dans certains cas, vous souhaitez associer un ou plusieurs formulaires à un dossier spécifique. Par exemple, les employés de votre organisation pourraient s’un dossier de rapport de progression dans leur banque de messages personnels pour la création et le stockage des rapports de progression. Étant donné que le rapport de progression est spécifique à un dossier de rapport de progression de chaque utilisateur, il n’est peut-être pas approprié stocker le formulaire de rapport de progression dans la bibliothèque de formulaires à l’échelle du système. Toutefois, une copie du formulaire de rapport de progression permettre être conservée dans la table de contenu associée du dossier de rapport de progression de chaque utilisateur. Cela empêche l’utilisateur d’utiliser des formulaires de rapport d’avancement en dehors du dossier désigné.
  
De façon conceptuelle, il est une bibliothèque de formulaires de dossier pour tous les dossiers dans une banque de messages, même si aucun serveur de formulaire n’est installés dans ce. Bibliothèques de formulaires dossier sont implémentées comme autres bibliothèques de formulaires, elles sont stockées en tant que tables de contenu associé dans le composant de substitution du dossier. Étant donné que les bibliothèques de formulaires dossier sont contenus dans le dossier, ils sont copiés ainsi que dans les opérations de copie de leur dossier parent.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

