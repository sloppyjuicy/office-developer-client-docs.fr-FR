---
title: Mode, propriété (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f30dac303541b0f53d06eb7756739ff1add6ce0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288868"
---
# <a name="mode-property-ado"></a><span data-ttu-id="cf0b4-102">Mode, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf0b4-102">Mode property (ADO)</span></span>


<span data-ttu-id="cf0b4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf0b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf0b4-104">Indique les autorisations disponibles pour la modification des données d'un objet [Connection](connection-object-ado.md), [Enregistrement](record-object-ado.md) ou [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cf0b4-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cf0b4-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="cf0b4-105">Settings and return values</span></span>

<span data-ttu-id="cf0b4-p101">Définit ou renvoie une valeur [ConnectModeEnum](connectmodeenum.md). La valeur par défaut d’un objet **Connexion** est **adModeUnknown**. La valeur par défaut d’un objet **Record** est **adModeRead**. La valeur par défaut d’un **Stream** associé à une source sous-jacente (ouverte avec une URL pour source ou comme **Stream** par défaut d’un objet **Record**) est **adModeRead**. La valeur par défaut d’un **Stream** non associé à une source sous-jacente (instanciée en mémoire) est **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf0b4-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf0b4-111">Remarks</span></span>

<span data-ttu-id="cf0b4-p102">Utilisez la propriété **Mode** pour définir ou pour renvoyer les autorisations d'accès utilisées par le fournisseur sur la connexion actuelle. Vous ne pouvez définir la propriété **Mode** que lorsque l'objet **Connection** est fermé.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="cf0b4-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="cf0b4-116">Cette propriété est accessible en lecture/écriture lorsque l'objet est fermé, mais en lecture seule alors qu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="cf0b4-117">**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet Connection côté client, la propriété **mode** peut uniquement être définie sur **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

