---
title: Méthode QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a0fbc93ab07df4f21c9b4df13454455ed3c48a82
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925190"
---
# <a name="querydefclose-method-dao"></a>Méthode QueryDef.Close (DAO)


**S’applique à**: Access 2013, Office 2013

Ferme un objet **QueryDef** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* . Fermer

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

Si l'objet **QueryDef** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.

Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

