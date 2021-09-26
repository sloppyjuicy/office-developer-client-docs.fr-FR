---
title: GetString, méthode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: efb5997e7b194d06d9facd5eeb1874d1d3286764
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618097"
---
# <a name="getstring-method-ado"></a>GetString, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Retourne l’objet [Recordset](recordset-object-ado.md) sous la forme d’une chaîne.

## <a name="syntax"></a>Syntaxe

*Variant*  =  *recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Valeur renvoyée

Retourne l'objet **Recordset** sous la forme d'un type **Variant** avec une valeur de chaîne (BSTR).

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*StringFormat* |Valeur [StringFormatEnum](stringformatenum.md) qui spécifie comment l’objet **Recordset** doit être converti en chaîne. Les paramètres  *DélimiteurLigne*, *DélimiteurColonne* et *ExprNull* sont utilisés uniquement avec un paramètre *FormatChaîne* affecté de la valeur **adClipString**.|
|*NumRows* |Facultatif. Nombre de lignes à convertir dans l'objet **RecordSet**. Dans le cas où *NbLignes* n'est pas spécifié ou s'il est supérieur au nombre total de lignes dans l'objet **RecordSet**, toutes les lignes de l'objet **RecordSet** sont converties.|
|*ColumnDelimiter* |Facultatif. Délimiteur utilisé entre les colonnes, s'il est spécifié ; sinon, le caractère de tabulation.|
|*RowDelimiter* |Facultatif. Délimiteur utilisé entre les lignes, s'il est spécifié ; sinon, le caractère de retour chariot.|
|*NullExpr* |Facultatif. Expression utilisée à la place d'une valeur NULL, si elle est spécifiée ; sinon, la chaîne vide.|

## <a name="remarks"></a>Remarques

Les données de ligne, mais pas les données de schéma, sont enregistrées dans la chaîne. Il est donc impossible de rouvrir un objet **Recordset** à l'aide de cette chaîne.

Cette méthode est équivalente à la méthode **GetClipString** RDO.

