---
title: Mode de traitement par lots (référence de base de données du bureau Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861201"
---
# <a name="batch-mode"></a><span data-ttu-id="c2c13-102">Mode Batch</span><span class="sxs-lookup"><span data-stu-id="c2c13-102">Batch Mode</span></span>


<span data-ttu-id="c2c13-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2c13-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2c13-p101">Le mode de mise à jour par lot est utilisé lorsque la propriété **LockType** a la valeur **adLockBatchOptimistic** et que la mise à jour par lot est prise en charge par le fournisseur. Certains paramètres de verrouillage ne sont pas disponibles en fonction de l'emplacement du curseur. Par exemple, un type de verrouillage pessimiste n'est pas disponible lorsque **CursorLocation** a la valeur **adUseClient**. À l'inverse, il se peut qu'un fournisseur ne prenne pas en charge un verrouillage optimiste du traitement par lot lorsque le curseur est positionné sur le serveur. Vous devez utiliser la mise à jour par lot uniquement avec un jeu de clés ou un curseur statique.</span><span class="sxs-lookup"><span data-stu-id="c2c13-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="c2c13-p102">La méthode **UpdateBatch** est utilisée pour envoyer les modifications de l'objet **Recordset** contenues dans le tampon de copie au serveur, afin de mettre à jour la source de données. La section suivante illustre l'ouverture d'un objet **Recordset** en mode de mise à jour par lot, la modification du tampon de copie puis l'envoi des modifications à la source de données par un appel à la méthode **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="c2c13-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="c2c13-111">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2c13-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="c2c13-112">Envoi des mises à jour : UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="c2c13-112">Sending the Updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)

- [<span data-ttu-id="c2c13-113">Filtrage des enregistrements mis à jour</span><span class="sxs-lookup"><span data-stu-id="c2c13-113">Filtering for Updated Records</span></span>](filtering-for-updated-records.md)

- [<span data-ttu-id="c2c13-114">Traitement des échecs de mise à jour</span><span class="sxs-lookup"><span data-stu-id="c2c13-114">Dealing with Failed Updates</span></span>](dealing-with-failed-updates.md)

- [<span data-ttu-id="c2c13-115">Détection et résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c2c13-115">Detecting and Resolving Conflicts</span></span>](detecting-and-resolving-conflicts.md)

- [<span data-ttu-id="c2c13-116">Déconnexion et reconnexion du recordset</span><span class="sxs-lookup"><span data-stu-id="c2c13-116">Disconnecting and Reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)

- [<span data-ttu-id="c2c13-117">Mise à jour des résultats d'une opération JOIN  : Unique Table</span><span class="sxs-lookup"><span data-stu-id="c2c13-117">Updating JOINed Results: Unique Table</span></span>](updating-joined-results-unique-table.md)

