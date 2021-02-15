---
title: Error Object - ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a7c77a59368851f43b5e7bf2275f9f282546fb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293482"
---
# <a name="error-object-ado"></a>Error, objet (ADO)


**S’applique à** : Access 2013, Office 2013

Contient des détails sur les erreurs d'accès aux données relatives à une seule opération impliquant le fournisseur.

## <a name="remarks"></a>Remarques

Toute opération impliquant des objets ADO peut générer une ou plusieurs erreurs liées au fournisseur. Lorsqu'une erreur se produit, un ou plusieurs objets **Error** sont placés dans la collection [Errors](errors-collection-ado.md) de l'objet [Connection](connection-object-ado.md). Lorsqu'une autre opération ADO génère une erreur, la collection **Errors** est vidée de son contenu ; le nouveau jeu d'objets **Error** est placé dans la collection **Errors**.

> [!NOTE]
> [!REMARQUE] Chaque objet **Error** représente une erreur de fournisseur spécifique, et pas une erreur ADO. Les erreurs ADO sont exposées au mécanisme de gestion des exceptions d'exécution. Par exemple, dans Microsoft Visual Basic, l'occurrence d'une erreur ADO spécifique déclenchera un événement **On Error** et apparaîtra dans l'objet **Error**. Pour obtenir la liste complète des erreurs ADO, voir la rubrique [ErrorValueEnum](errorvalueenum.md).

Vous pouvez lire les propriétés d'un objet **Error** pour obtenir des détails spécifiques sur chaque erreur, notamment les suivantes :

- la propriété [Description](description-property-ado.md), qui contient le texte de l'erreur (propriété par défaut) ;

- la propriété [Number](number-property-ado.md), qui contient l'entier **Long** de la constante de l'erreur ;

- la propriété [Source](source-property-ado-error.md), qui identifie l'objet ayant entraîné l'erreur et est particulièrement utile lorsque vous avez plusieurs objets **Error** dans la collection **Errors** à la suite d'une demande exécutée sur une source de données ;

- les propriétés [SQLState](sqlstate-property-ado.md) et [NativeError](nativeerror-property-ado.md), qui fournissent des informations depuis des sources de données SQL.

Lorsqu'une erreur liée au fournisseur se produit, elle est placée dans la collection **Errors** de l'objet **Connection**. ADO prend en charge le renvoi de plusieurs erreurs par une seule opération ADO pour la prise en charge des informations d'erreur spécifiques au fournisseur. Pour obtenir ce niveau élevé de détail dans un gestionnaire d'erreurs, utilisez les fonctions d'interception appropriées de la langue ou de l'environnement dans lesquels vous travaillez, puis utilisez des boucles imbriquées pour énumérer les propriétés de chaque objet **Error** dans la collection **Errors**.

**Utilisateurs Microsoft Visual Basic et VBScript** S’il n’existe aucun objet **Connection** valide, vous devez récupérer les informations d’erreur de **l’objet Error.**

Tout comme le font les fournisseurs, ADO efface l'objet **OLE Error Info** avant de lancer un appel susceptible de générer une nouvelle erreur spécifique du fournisseur. Toutefois, les objets présents dans la collection **Errors** sur l'objet **Connection** sont effacés et de nouveaux objets ne lui sont ajoutés que si le fournisseur génère une nouvelle erreur ou si la méthode [Clear](clear-method-ado.md) est appelée.

Certaines propriétés et méthodes renvoient des avertissements qui s'affichent sous la forme d'objets **Error** dans la collection **Errors**, mais qui n'empêchent pas l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md), la méthode [Open](open-method-ado-connection.md) sur un objet **Connection** ou avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ceci vous permet de lire la propriété [Count](count-property-ado.md) de la collection **Errors** pour tester les avertissements renvoyés.

