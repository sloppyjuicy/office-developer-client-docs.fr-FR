---
title: GetChildren, méthode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6c2c23ed24ecde11e182e623834f986a37b9e73f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573004"
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

