---
title: Supports, méthode (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9551120657b2284959f1f7c69d8a11324ea9e5e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585255"
---
# <a name="supports-method-ado"></a>Supports, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Détermine si un objet [Recordset](recordset-object-ado.md) spécifié prend en charge un type de fonctionnalité particulier.

## <a name="syntax"></a>Syntaxe

*booléen*  =  *recordset*. Supports (*CursorOptions*)

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Boolean** indiquant si toutes les fonctionnalités identifiées par l’argument *CursorOptions* sont prises en charge par le fournisseur.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*CursorOptions* |Expression de type **Long** comportant une ou plusieurs valeurs [CursorOptionEnum](cursoroptionenum.md).|

## <a name="remarks"></a>Remarques

Utilisez la méthode **Supports** pour déterminer les types de fonctionnalités prises en charge par un objet **Recordset**. Si l'objet **Recordset** prend en charge les fonctionnalités dont les constantes correspondantes se trouvent dans *CursorOptions*, la méthode **Supports** retourne **True**. Sinon, elle renvoie **False**.


> [!NOTE]
> [!REMARQUE] Même si la méthode **Supports** peut retourner la valeur **True** pour une fonctionnalité déterminée, cela ne signifie pas pour autant que le fournisseur peut rendre la fonctionnalité disponible en toutes circonstances. La méthode **Supports** indique simplement si le fournisseur peut prendre en charge la fonctionnalité spécifiée, en partant du principe que certaines conditions sont remplies. Par exemple, la méthode **Supports** peut indiquer qu'un objet **Recordset** prend en charge les mises à jour même si le curseur est basé sur une jointure de plusieurs tables, dont certaines colonnes ne peuvent pas être mises à jour.


