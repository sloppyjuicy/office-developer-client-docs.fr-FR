---
title: CreateParameter, méthode (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: ee1103492c6a637463002070239fbdafbe98578e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589812"
---
# <a name="createparameter-method-ado"></a>CreateParameter, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Crée un objet [Parameter](parameter-object-ado.md) avec les propriétés spécifiées.

## <a name="syntax"></a>Syntaxe

**Commande Définir** *un*  =  *paramètre.* CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)

## <a name="return-value"></a>Valeur renvoyée

Retourne un objet **Parameter**.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Name* |Facultatif. Valeur de type **String** contenant le nom de l'objet **Parameter**.|
|*Type* |Facultatif. Valeur [DataTypeEnum](datatypeenum.md) qui spécifie le type de données de l'objet **Parameter**.|
|*Direction* |Facultatif. Valeur [ParameterDirectionEnum](parameterdirectionenum.md) qui spécifie le type de l'objet **Parameter**.|
|*Size* |Facultatif. Valeur de type **Long** qui spécifie la longueur maximale de la valeur du paramètre en caractères ou en octets.|
|*Value* |Facultatif. **Variant** qui spécifie la valeur de l'objet **Parameter**.|

## <a name="remarks"></a>Remarques

Utilisez la méthode **CreateParameter** pour créer un objet **Parameter** avec un nom, un type, une direction, une taille et une valeur spécifiques. Toutes les valeurs passées dans les arguments sont écrites dans les propriétés **Parameter** correspondantes.

Cette méthode n'ajoute pas automatiquement l'objet **Parameter** à la collection **Parameters** d'un objet [Command](command-object-ado.md). Ceci vous permet de définir des propriétés supplémentaires dont ADO validera les valeurs lorsque vous ajouterez l'objet **Parameter** à la collection.

Si vous spécifiez un type de données de longueur variable dans l’argument *Type*, vous devez passer un argument *Size* ou définir la propriété [Size](size-property-ado.md) de l’objet **Parameter** avant d’ajouter cet objet à la collection **Parameters**. Sinon, une erreur se produit.

Si vous spécifiez un type de données numérique (**adNumeric** ou **adDecimal**) dans l’argument *Type*, vous devez également définir les propriétés [NumericScale](numericscale-property-ado.md) et [Precision](precision-property-ado.md).

