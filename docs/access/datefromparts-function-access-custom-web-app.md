---
title: Fonction DateFromParts (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Retourne une valeur de date pour l’année, le mois et le jour spécifiés.
ms.openlocfilehash: b8411c0a47824ab8331d1941eac2b4d03d685d83
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893836"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (Access custom web app)

Retourne une valeur de date pour l’année, le mois et le jour spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**DateFromParts** (*Année*, *Mois*, *Jour*)
  
La fonction **DateFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression entière spécifiant une année. |
| *Month*  <br/> |Expression entière spécifiant un mois, de 1 à 12. |
| *Day*  <br/> |Expression entière spécifiant un jour. |

## <a name="remarks"></a>Remarques

**DateFromParts** retourne une valeur de date avec la partie date définie sur l’année, le mois et le jour spécifiés, et la partie heure définie sur la valeur par défaut. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments requis sont null, null est retourné.
  
## <a name="example"></a>Exemple

L’expression suivante utilise la fonction **DateFromParts** pour calculer le premier jour du mois en cours.
  
`DateFromParts(Year(Today()),Month(Today()),1)`
