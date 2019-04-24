---
title: IsolationLevel, propriété (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291148"
---
# <a name="isolationlevel-property-ado"></a>IsolationLevel, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le niveau d'isolation d'un objet [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [IsolationLevelEnum](isolationlevelenum.md). La valeur par défaut est **adXactChaos**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **IsolationLevel** pour définir le niveau d'isolation d'un objet **Connection**. Le paramètre ne prend effet qu'à l'appel suivant de la méthode [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si le niveau d'isolation que vous demandez n'est pas disponible, le fournisseur peut renvoyer le meilleur niveau d'isolation suivant.

La propriété **IsolationLevel** est en accessible lecture et en écriture.

**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet Connection côté client, la propriété **IsolationLevel** ne peut être définie que sur **adXactUnspecified**.

Parce que les utilisateurs travaillent avec des objets **Recordset** déconnectés, stockés dans un cache client, il peut y avoir des problèmes liés à la multiplicité des utilisateurs. Par exemple lorsque deux utilisateurs différents tentent de mettre à jour le même enregistrement, Remote Data Service exécute la mise à jour de l'utilisateur dont la requête lui parvient en premier. La demande de mise à jour du second utilisateur échoue et une erreur est générée.

