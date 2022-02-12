---
title: Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: 97cebaed4659ff12621e08cdb58af7353cca6b18
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782877"
---
# <a name="parse-function-access-custom-web-app"></a>Parse Function (Access custom web app)

Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**Analyse** (*TextExpression*, *DataType*)
  
La **fonction Parse** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié. |
| *DataType*  <br/> |Valeur littérale représentant le type de données demandé pour le résultat. |
   
## <a name="remarks"></a>Remarques

Utilisez **l’utilisation de l’exemple** uniquement pour la conversion de chaînes en types de date/heure et de nombre. Pour les conversions de type général, utilisez **la fonction Convert** . Gardez à l’esprit qu’il existe une certaine surcharge de performances lors de l’l’exécution de l’une des valeurs de chaîne.
  