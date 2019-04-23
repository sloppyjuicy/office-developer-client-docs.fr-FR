---
title: Parameter, objet (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288076"
---
# <a name="parameter-object-ado"></a>Parameter, objet (ADO)


**S’applique à** : Access 2013, Office 2013

Représente un paramètre ou un argument associé à un objet [Command](command-object-ado.md) basé sur une requête paramétrée ou sur une procédure stockée.

## <a name="remarks"></a>Remarques

De nombreux fournisseurs prennent en charge les commandes paramétrées. Ces dernières sont des commandes dans lesquelles l'action désirée est définie une fois, mais qui comportent des variables (ou paramètres) permettant d'en modifier certains aspects. Par exemple, une instruction SQL SELECT peut utiliser un paramètre pour définir les critères de correspondance d'une clause WHERE, et un autre définissant le nom de colonne pour une clause SORT BY.

Les objets **Parameter** représentent des paramètres associés à des requêtes paramétrées, ou les arguments d'entrée/sortie et les valeurs de retour de procédures stockées. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Parameter** risquent de ne pas être disponibles.

Les collections, les méthodes et les propriétés d'un objet **Parameter** vous permettent d'effectuer diverses tâches :

  - définir ou renvoyer le nom d'un paramètre avec la propriété [Name](name-property-ado.md) ;

  - définir ou renvoyer la valeur d'un paramètre avec la propriété [Value](value-property-ado.md) ( **Value** étant la propriété par défaut de l'objet **Parameter** ) ;

  - définir ou renvoyer les caractéristiques des paramètres avec les propriétés [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) et [Type](type-property-ado.md) ;

  - passer des données binaires longues ou de caractères à un paramètre avec la méthode [AppendChunk](appendchunk-method-ado.md) :

  - accéder aux attributs spécifiques d'un fournisseur avec la collection [Properties](properties-collection-ado.md).

Si vous connaissez les noms et les propriétés des paramètres associés à la procédure stockée ou à la requête paramétrée que vous voulez appeler, vous pouvez utiliser la méthode [CreateParameter](createparameter-method-ado.md) pour créer des objets **Parameter** avec les paramètres de propriété appropriés et utiliser la méthode [Append](append-method-ado.md) pour les ajouter à la collection [Parameters](parameters-collection-ado.md). Cela vous permet de définir et de renvoyer des valeurs de paramètres sans avoir à appeler la méthode [Refresh](refresh-method-ado.md) sur la collection **Parameters** pour récupérer les informations de paramètres auprès du fournisseur, opération potentiellement gourmande en ressources.

