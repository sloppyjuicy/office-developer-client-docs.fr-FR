---
title: Mode, propriété (ADO)
TOCTitle: Mode Property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d258623756b53a82c06320185f9b75247087b2d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469079"
---
# <a name="mode-property-ado"></a>Mode, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique les autorisations disponibles pour la modification des données d'un objet [Connection](connection-object-ado.md), [Enregistrement](record-object-ado.md) ou [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [ConnectModeEnum](connectmodeenum.md). La valeur par défaut d’un objet **Connexion** est **adModeUnknown**. La valeur par défaut d’un objet **Record** est **adModeRead**. La valeur par défaut d’un **Stream** associé à une source sous-jacente (ouverte avec une URL pour source ou comme **Stream** par défaut d’un objet **Record**) est **adModeRead**. La valeur par défaut d’un **Stream** non associé à une source sous-jacente (instanciée en mémoire) est **adModeUnknown**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Mode** pour définir ou pour renvoyer les autorisations d'accès utilisées par le fournisseur sur la connexion actuelle. Vous ne pouvez définir la propriété **Mode** que lorsque l'objet **Connection** est fermé.

Un objet **Stream** , si le mode d’accès n’est pas spécifié, il est hérité de la source utilisée pour ouvrir l’objet **Stream** . Par exemple, si un **flux** est ouvert à partir d’un objet **Record** , par défaut il est ouvert dans le même mode que l' **enregistrement**.

Cette propriété est accessible en lecture/écriture lorsque l'objet est fermé, mais en lecture seule alors qu'il est ouvert.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de connexion côté client, la propriété **Mode** peut uniquement être définie **: adModeUnknown**.

