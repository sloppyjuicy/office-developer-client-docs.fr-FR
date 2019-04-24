---
title: Errors, collection (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293426"
---
# <a name="errors-collection-ado"></a>Errors, collection (ADO)


**S’applique à** : Access 2013, Office 2013

Contient tous les objets [Error](error-object-ado.md) créés en réponse à une erreur liée au fournisseur.

## <a name="remarks"></a>Remarques

Toute opération impliquant des objets ADO peut générer une ou plusieurs erreurs d'un fournisseur. Lorsqu'une erreur se produit, un ou plusieurs objets **Error** peuvent être placés dans la collection **Errors** de l'objet [Connection](connection-object-ado.md). Lorsqu'une autre opération ADO génère une erreur, la collection **Errors** est vidée de son contenu, et le nouveau jeu d'objets **Error** peut être placé dans la collection **Errors**.

Chaque objet **Error** représente une erreur de fournisseur spécifique, et pas une erreur ADO. Les erreurs ADO sont exposées au mécanisme de gestion des exceptions d'exécution. Par exemple, dans Microsoft Visual Basic, l'occurrence d'une erreur ADO spécifique déclenchera un événement [onError](onerror-event-rds.md) et apparaîtra dans l'objet **Err**.

Les opérations ADO qui ne génèrent pas d'erreur sont sans effet sur la collection **Errors**. Utilisez la méthode [Clear](clear-method-ado.md) pour effacer manuellement le contenu de la collection **Errors**.

Le jeu d'objets **Error** de la collection **Errors** décrit toutes les erreurs qui ont eu lieu en réponse à une seule instruction. Le fait d'énumérer les erreurs spécifiques dans la collection **Errors** permet à vos routines de gestion des erreurs de déterminer avec plus de précision la cause et l'origine d'une erreur et d'exécuter les actions appropriées pour la corriger.

Certaines propriétés et méthodes renvoient des avertissements qui s'affichent sous la forme d'objets **Error** dans la collection **Errors**, mais qui n'empêchent pas l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md), la méthode [Open](open-method-ado-connection.md) sur un objet **Connection** ou avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ceci vous permet de lire la propriété [Count](count-property-ado.md) de la collection **Errors** pour tester les avertissements renvoyés.


> [!NOTE]
> [!REMARQUE] Pour plus d'informations sur la manière dont une seule opération ADO peut générer plusieurs erreurs, voir la rubrique consacrée à l'objet **Error**.


