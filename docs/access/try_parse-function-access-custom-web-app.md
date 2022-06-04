---
title: Try_Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analyse une valeur de texte au type de données spécifié dans la culture de l’application ou retourne la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: f331e44d3e962a6c15b8c24d955a7f9e2afcf15c
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894683"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse Function (Access custom web app)

Analyse une valeur de texte au type de données spécifié dans la culture de l’application ou retourne la valeur Null si la conversion n’est pas valide.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

 **Try_Parse** (*TextExpression*, *DataType*)
  
La fonction **Try_Parse** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié. |
| *DataType*  <br/> |Type de données dans lequel analyser *TextExpression*. |

## <a name="remarks"></a>Remarques

Utilisez **Try_Parse** uniquement pour la conversion de chaîne en types date/heure et nombre. Pour les conversions de type général, continuez à utiliser **Convert**.
  