---
title: Mode, propriété (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 166f214eb43cb8aafed63e1f17a013a71d51ac08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606582"
---
# <a name="mode-property-ado"></a>Mode, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique les autorisations disponibles pour la modification des données d'un objet [Connection](connection-object-ado.md), [Enregistrement](record-object-ado.md) ou [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [ConnectModeEnum](connectmodeenum.md). La valeur par défaut d’un objet **Connexion** est **adModeUnknown**. La valeur par défaut d’un objet **Record** est **adModeRead**. La valeur par défaut d’un **Stream** associé à une source sous-jacente (ouverte avec une URL pour source ou comme **Stream** par défaut d’un objet **Record**) est **adModeRead**. La valeur par défaut d’un **Stream** non associé à une source sous-jacente (instanciée en mémoire) est **adModeUnknown**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Mode** pour définir ou pour renvoyer les autorisations d'accès utilisées par le fournisseur sur la connexion actuelle. Vous ne pouvez définir la propriété **Mode** que lorsque l'objet **Connection** est fermé.

For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.

Cette propriété est accessible en lecture/écriture lorsque l'objet est fermé, mais en lecture seule alors qu'il est ouvert.

**Utilisation du service de données à distance** Lorsqu’elle est utilisée sur un objet Connection côté client, la propriété **Mode** ne peut être définie que sur **adModeUnknown**.

