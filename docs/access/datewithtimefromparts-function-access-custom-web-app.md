---
title: Fonction DateWithTimeFromParts (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Retourne une date et une heure en fonction d’une année, d’un mois, d’un jour et d’une heure spécifiés.
ms.openlocfilehash: 1fff59f613c0cb273eb7b0b98d8f37a2eb2cf8c1
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893786"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Fonction DateWithTimeFromParts (Access custom web app)

Retourne une date et une heure en fonction d’une année, d’un mois, d’un jour et d’une heure spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/online/overview)
  
## <a name="syntax"></a>Syntaxe

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)
  
La fonction **DateWithTimeFromParts** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression entière spécifiant une année. |
| *Month*  <br/> |Expression entière spécifiant un mois. |
| *Day*  <br/> |Expression entière spécifiant un jour. |
| *Hour*  <br/> |Expression entière spécifiant des heures. |
| *Minute*  <br/> |Expression entière spécifiant des minutes. |
| *Second*  <br/> |Expression entière spécifiant des secondes. |

## <a name="remarks"></a>Remarques

**DateWithTimeFromParts** retourne une valeur date/heure entièrement initialisée. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments requis sont Null, null est retourné.
  