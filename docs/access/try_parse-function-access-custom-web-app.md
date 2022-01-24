---
title: Try_Parse Function (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analyse une valeur de texte au type de données spécifié dans la culture de l’application ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: ebf27eabc97680439c0700cc0b3f6e584e5771cf
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179913"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse Function (Application web personnalisée Access)

Analyse une valeur de texte au type de données spécifié dans la culture de l’application ou renvoie la valeur Null si la conversion n’est pas valide.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **Try_Parse** (*TextExpression*, *DataType*)
  
La **Try_Parse** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Type de données dans lequel vous analysez *TextExpression*.  <br/> |

## <a name="remarks"></a>Remarques

Utilisez **Try_Parse** uniquement pour la conversion de chaîne en types de date/heure et de nombre. Pour les conversions de type général, continuez à utiliser **Convert**.
  