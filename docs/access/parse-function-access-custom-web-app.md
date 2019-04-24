---
title: Fonction d'analyse (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analyse une valeur de texte et retourne sa valeur dans un type donné à l'aide de la culture de l'application.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308056"
---
# <a name="parse-function-access-custom-web-app"></a>Fonction d'analyse (application Web personnalisée Access)

Analyse une valeur de texte et retourne sa valeur dans un type donné à l'aide de la culture de l'application.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Analyser** (*TextExpression*, *DataType*) 
  
La fonction d' **analyse** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Valeur littérale représentant le type de données demandé pour le résultat.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez l' **analyse** uniquement pour convertir une chaîne en type de date/heure et de nombre. Pour les conversions de type générales, utilisez la fonction **Convert** . Gardez à l'esprit qu'il existe une certaine charge de performances dans l'analyse de la valeur de chaîne. 
  

