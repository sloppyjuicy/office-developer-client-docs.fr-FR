---
title: Propriété Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ad1428d9a820a2489a9051ca77c0de854e03d57
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920850"
---
# <a name="recordset2updateoptions-property-dao"></a>Propriété Recordset2.UpdateOptions (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . UpdateOptions (OptionsMAJ)

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Lorsqu'une méthode **[Update](recordset2-update-method-dao.md)** en mode de traitement par lot est exécutée, DAO et la bibliothèque client de curseurs par lots créent une série d'instructions SQL UPDATE pour apporter les modifications nécessaires. Une clause SQL WHERE est créée pour chaque mise à jour afin d'isoler les enregistrements marqués comme étant modifiés par la propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)**. Dans la mesure où certains serveurs distants utilisent des déclencheurs ou d'autres moyens pour appliquer l'intégrité référentielle, il est souvent essentiel de limiter les champs à mettre à jour aux seuls champs affectés par la modification. 

Pour ce faire, affectez à la propriété **UpdateOptions** l'une des constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**. De cette façon, seule la partie minimale indispensable du code de déclencheur est exécutée. Ainsi, l'opération de mise à jour est exécutée plus rapidement et est moins susceptible de contenir des erreurs.

h **dbCriteriaDeleteInsert** **dbCriteriaUpdate** **UpdateOptions**

Si vous ne spécifiez pas de constantes, **dbCriteriaUpdate** et **dbCriteriaKey** seront utilisées.

Dans la mesure où les enregistrements récemment ajoutés génèrent toujours des instructions INSERT et les enregistrements supprimés toujours des instructions DELETE, cette propriété ne concerne que la façon dont la bibliothèque de curseurs met à jour les enregistrements modifiés.

