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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722024"
---
# <a name="getchildren-method-ado"></a>GetChildren, méthode (ADO)


**S’applique à**: Access 2013, Office 2013


Retourne un objet [Recordset](recordset-object-ado.md) dont les lignes représentent les enfants d'un objet [Record](record-object-ado.md) d'une collection.

## <a name="syntax"></a>Syntaxe

**La valeur** *jeu d’enregistrements*  =  *enregistrement*. GetChildren

## <a name="return-value"></a>Valeur renvoyée

Objet **Recordset** dont chaque ligne représente un enfant de l'objet **Record** actif. Par exemple, les enfants d'un objet **Record** qui représente un répertoire, sont les fichiers et sous-répertoires contenus dans le répertoire parent.

## <a name="remarks"></a>Notes

Le fournisseur détermine les colonnes qui figureront dans l'objet **Recordset** retourné. Par exemple, un fournisseur de source de documents retourne toujours un objet **Recordset** de ressource.

