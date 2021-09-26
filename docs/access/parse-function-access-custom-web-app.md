---
title: Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: e09478cee26accd8e316d3de36d8034f0ca02526
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631537"
---
# <a name="parse-function-access-custom-web-app"></a>Parse Function (Access custom web app)

Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas l’ajouter pour le *\<service\> moment. Veuillez essayer à nouveau plus tard.* > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Parse** (*TextExpression*, *DataType*) 
  
La **fonction Parse** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Valeur littérale représentant le type de données demandé pour le résultat.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **l’utilisation d’Parse** uniquement pour la conversion de chaîne en types de date/heure et de nombre. Pour les conversions de type général, utilisez **la fonction Convert.** Gardez à l’esprit qu’il existe une certaine surcharge de performances lors de l’exécution de l’une des valeurs de chaîne. 
  

