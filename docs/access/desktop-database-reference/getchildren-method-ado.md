---
title: GetChildren, méthode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292306"
---
# <a name="getchildren-method-ado"></a>GetChildren, méthode (ADO)


**S’applique à** : Access 2013, Office 2013


Retourne un objet [Recordset](recordset-object-ado.md) dont les lignes représentent les enfants d’un objet [Record](record-object-ado.md) d’une collection.

## <a name="syntax"></a>Syntaxe

**Définissez** *l’enregistrement du jeu*  =  *d’enregistrements.* GetChildren

## <a name="return-value"></a>Valeur renvoyée

Objet **Recordset** dont chaque ligne représente un enfant de l'objet **Record** actif. Par exemple, les enfants d'un objet **Record** qui représente un répertoire, sont les fichiers et sous-répertoires contenus dans le répertoire parent.

## <a name="remarks"></a>Remarques

Le fournisseur détermine les colonnes qui figureront dans l'objet **Recordset** retourné. Par exemple, un fournisseur de source de documents retourne toujours un objet **Recordset** de ressource.

