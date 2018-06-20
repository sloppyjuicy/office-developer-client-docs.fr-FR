---
title: Analyser la fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analyse d’une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781962"
---
# <a name="parse-function-access-custom-web-app"></a>Analyser la fonction (accès personnalisé web app)

Analyse d’une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Analyser** (*TextExpression*, *type de données*) 
  
La fonction **Parse** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Une expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Valeur littérale qui représente le type de données demandé pour le résultat.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **analyser** uniquement pour réaliser la conversion d’une chaîne de date/heure et types de numéros. Pour les conversions de type général, utilisez la fonction **Convert** . N’oubliez pas qu’il existe certaines performances une surcharge de l’analyse de la valeur de chaîne. 
  

