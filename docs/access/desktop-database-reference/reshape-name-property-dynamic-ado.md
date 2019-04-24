---
title: Reshape Name, propriété dynamique (ADO)
TOCTitle: Reshape Name dynamic property (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b606960238e2f9a08d034ed92a79f7a767a1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306600"
---
# <a name="reshape-name-dynamic-property-ado"></a>Reshape Name, propriété dynamique (ADO)


**S’applique à** : Access 2013, Office 2013

Spécifie un nom pour l'objet [Recordset](recordset-object-ado.md).

## <a name="return-values"></a>Valeurs de retour

Renvoie une valeur de type **String** qui représente le nom de l'objet **Recordset**.

## <a name="remarks"></a>Remarques

Les noms persistent pendant la durée de la connexion ou jusqu'à la fermeture de l'objet **Recordset**.

La propriété **Reshape Name** est principalement destinée à une utilisation avec la fonction de remise en forme du fournisseur de services [Service de mise en forme des données pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md). Les noms doivent être uniques pour participer à la remise en forme.

Cette propriété est en lecture seule, mais elle peut être définie indirectement lorsqu'un objet Recordset est créé. Par exemple, si une clause d'une commande SHAPE crée un objet Recordset et lui donne un nom d'alias avec le mot clé « AS », l'alias est affecté à la propriété Reshape Name. Si aucun alias n'est déclaré, la propriété Reshape Name est affectée d'un nom unique généré par le service de mise en forme des données. Si le nom d'alias est identique au nom d'un objet **Recordset** existant, aucun des deux objets **Recordset** ne peut être mis en forme tant que l'un d'eux n'a pas été libéré. Le comportement par défaut peut être modifié en affectant à la propriété « Unique Reshape Names » (voir la section "Service de mise en forme des données Microsoft pour OLE DB ») de la connexion ADO la valeur TRUE. Le service de mise en forme des données peut alors modifier les noms affectés par l'utilisateur, si cela s'avère nécessaire pour des raisons d'unicité.

Utilisez la propriété **Reshape Name** lorsque vous souhaitez faire référence à un objet **Recordset** dans une commande SHAPE ou lorsque vous ignorez son nom car il a été généré par le service de mise en forme des données. Dans ce cas, vous pouvez générer une commande SHAPE en concaténant la commande autour de la chaîne renvoyée par la propriété **Reshape Name**.

La propriété **Reshape Name** est une propriété dynamique ajoutée à la collection **Properties** de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

