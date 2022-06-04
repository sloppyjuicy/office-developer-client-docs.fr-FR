---
title: Fonction TimeFromParts (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Retourne une valeur d’heure en fonction des parties spécifiées.
ms.openlocfilehash: 089e0ebc33b6148f350ea35d5671c4d5cebfb22a
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893654"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Fonction TimeFromParts (Access custom web app)

Retourne une valeur d’heure en fonction des parties spécifiées.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

**TimeFromParts** (*Heure*, *Minute*, *Deuxième*)
  
La fonction **TimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Hour*  <br/> |Expression entière spécifiant des heures. |
| *Minute*  <br/> |Expression entière spécifiant des minutes. |
| *Second*  <br/> |Expression entière spécifiant des secondes. |

## <a name="see-also"></a>Voir aussi

 **TimeFromParts** retourne une valeur de temps entièrement initialisée. Si les arguments ne sont pas valides, une erreur est générée. Si l’un des paramètres est null, null est retourné.
  