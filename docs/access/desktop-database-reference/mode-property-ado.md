---
title: Mode, propriété (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74b0a401c5fbd7e34cbd002020d81b9b0858e4f7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874278"
---
# <a name="mode-property-ado"></a><span data-ttu-id="97a32-102">Mode, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="97a32-102">Mode property (ADO)</span></span>


<span data-ttu-id="97a32-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97a32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97a32-104">Indique les autorisations disponibles pour la modification des données d'un objet [Connection](connection-object-ado.md), [Enregistrement](record-object-ado.md) ou [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="97a32-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="97a32-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="97a32-105">Settings and return values</span></span>

<span data-ttu-id="97a32-p101">Définit ou renvoie une valeur [ConnectModeEnum](connectmodeenum.md). La valeur par défaut d’un objet **Connexion** est **adModeUnknown**. La valeur par défaut d’un objet **Record** est **adModeRead**. La valeur par défaut d’un **Stream** associé à une source sous-jacente (ouverte avec une URL pour source ou comme **Stream** par défaut d’un objet **Record**) est **adModeRead**. La valeur par défaut d’un **Stream** non associé à une source sous-jacente (instanciée en mémoire) est **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="97a32-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a32-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="97a32-111">Remarks</span></span>

<span data-ttu-id="97a32-p102">Utilisez la propriété **Mode** pour définir ou pour renvoyer les autorisations d'accès utilisées par le fournisseur sur la connexion actuelle. Vous ne pouvez définir la propriété **Mode** que lorsque l'objet **Connection** est fermé.</span><span class="sxs-lookup"><span data-stu-id="97a32-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="97a32-114">Un objet **Stream** , si le mode d’accès n’est pas spécifié, il est hérité de la source utilisée pour ouvrir l’objet **Stream** .</span><span class="sxs-lookup"><span data-stu-id="97a32-114">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object.</span></span> <span data-ttu-id="97a32-115">Par exemple, si un **flux** est ouvert à partir d’un objet **Record** , par défaut il est ouvert dans le même mode que l' **enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="97a32-115">For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="97a32-116">Cette propriété est accessible en lecture/écriture lorsque l'objet est fermé, mais en lecture seule alors qu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="97a32-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="97a32-117">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de connexion côté client, la propriété **Mode** peut uniquement être définie **: adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="97a32-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

