---
title: Mode de traitement par lots (référence de base de données du bureau Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717810"
---
# <a name="batch-mode"></a><span data-ttu-id="3aa6d-102">Mode Batch</span><span class="sxs-lookup"><span data-stu-id="3aa6d-102">Batch mode</span></span>

<span data-ttu-id="3aa6d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3aa6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3aa6d-p101">Le mode de mise à jour par lot est utilisé lorsque la propriété **LockType** a la valeur **adLockBatchOptimistic** et que la mise à jour par lot est prise en charge par le fournisseur. Certains paramètres de verrouillage ne sont pas disponibles en fonction de l'emplacement du curseur. Par exemple, un type de verrouillage pessimiste n'est pas disponible lorsque **CursorLocation** a la valeur **adUseClient**. À l'inverse, il se peut qu'un fournisseur ne prenne pas en charge un verrouillage optimiste du traitement par lot lorsque le curseur est positionné sur le serveur. Vous devez utiliser la mise à jour par lot uniquement avec un jeu de clés ou un curseur statique.</span><span class="sxs-lookup"><span data-stu-id="3aa6d-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="3aa6d-p102">La méthode **UpdateBatch** est utilisée pour envoyer les modifications de l'objet **Recordset** contenues dans le tampon de copie au serveur, afin de mettre à jour la source de données. La section suivante illustre l'ouverture d'un objet **Recordset** en mode de mise à jour par lot, la modification du tampon de copie puis l'envoi des modifications à la source de données par un appel à la méthode **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="3aa6d-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="3aa6d-111">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3aa6d-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="3aa6d-112">Envoi des mises à jour : UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="3aa6d-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="3aa6d-113">Filtrage des enregistrements mis à jour</span><span class="sxs-lookup"><span data-stu-id="3aa6d-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="3aa6d-114">Traitement des échecs de mise à jour</span><span class="sxs-lookup"><span data-stu-id="3aa6d-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="3aa6d-115">Détection et résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="3aa6d-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="3aa6d-116">Déconnexion et reconnexion du recordset</span><span class="sxs-lookup"><span data-stu-id="3aa6d-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="3aa6d-117">Mise à jour des résultats de la jonction : Unique Table</span><span class="sxs-lookup"><span data-stu-id="3aa6d-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

