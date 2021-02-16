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
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414283"
---
# <a name="folder-form-libraries"></a>Bibliothèques de formulaires de dossiers

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans certains cas, vous pouvez associer un ou plusieurs formulaires à un dossier spécifique. Par exemple, les employés de votre organisation peuvent tous avoir un dossier Rapport d’avancement dans leur magasin de messages personnels pour créer et stocker des rapports d’avancement. Étant donné que le rapport d’avancement est spécifique au dossier Rapport d’avancement de chaque utilisateur, il peut ne pas être approprié de stocker le formulaire de rapport d’avancement dans la bibliothèque de formulaires à l’échelle du système. Toutefois, une copie du formulaire de rapport d’avancement peut être conservée dans la table des matières associée du dossier Rapport d’avancement de chaque utilisateur. Cela empêche l’utilisateur d’utiliser des formulaires de rapport de progression en dehors du dossier désigné.
  
D’un point de vue conceptuel, il existe une bibliothèque de formulaires de dossiers pour chaque dossier d’une magasin de messages, même si aucun serveur de formulaire n’y est installé. Les bibliothèques de formulaires de dossiers sont implémentées comme d’autres bibliothèques de formulaires ; elles sont stockées en tant que tables de contenu associé dans l’autre partie du dossier. Étant donné que les bibliothèques de formulaires de dossiers sont contenues dans le dossier, elles sont copiées avec leur dossier parent dans les opérations de copie.
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

