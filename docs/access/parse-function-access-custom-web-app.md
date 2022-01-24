---
title: Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: 90625da589875d3876ec80156efb354855a3240d
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180382"
---
# <a name="parse-function-access-custom-web-app"></a>Parse Function (Access custom web app)

Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter *\<service\> immédiatement. Veuillez essayer à nouveau plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme Office [cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

**Parse** (*TextExpression*, *DataType*)
  
La **fonction Parse** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Valeur littérale représentant le type de données demandé pour le résultat.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **l’utilisation de l’exemple** uniquement pour la conversion de chaînes en types de date/heure et de nombre. Pour les conversions de type général, utilisez **la fonction Convert.** Gardez à l’esprit qu’il existe une certaine surcharge de performances lors de l’l’exécution de l’une des valeurs de chaîne.
  