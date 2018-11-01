---
title: Mode de traitement par lots (référence de base de données du bureau Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ee4805f89d6a6a9d114c4347d808be61683efe6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880613"
---
# <a name="batch-mode"></a>Mode Batch


**S’applique à**: Access 2013, Office 2013

Le mode de mise à jour par lot est utilisé lorsque la propriété **LockType** a la valeur **adLockBatchOptimistic** et que la mise à jour par lot est prise en charge par le fournisseur. Certains paramètres de verrouillage ne sont pas disponibles en fonction de l'emplacement du curseur. Par exemple, un type de verrouillage pessimiste n'est pas disponible lorsque **CursorLocation** a la valeur **adUseClient**. À l'inverse, il se peut qu'un fournisseur ne prenne pas en charge un verrouillage optimiste du traitement par lot lorsque le curseur est positionné sur le serveur. Vous devez utiliser la mise à jour par lot uniquement avec un jeu de clés ou un curseur statique.

La méthode **UpdateBatch** est utilisée pour envoyer les modifications de l'objet **Recordset** contenues dans le tampon de copie au serveur, afin de mettre à jour la source de données. La section suivante illustre l'ouverture d'un objet **Recordset** en mode de mise à jour par lot, la modification du tampon de copie puis l'envoi des modifications à la source de données par un appel à la méthode **UpdateBatch**.

Cette section comprend les rubriques suivantes :

- [Envoi des mises à jour : UpdateBatch](sending-the-updates-updatebatch.md)

- [Filtrage des enregistrements mis à jour](filtering-for-updated-records.md)

- [Traitement des échecs de mise à jour](dealing-with-failed-updates.md)

- [Détection et résolution des conflits](detecting-and-resolving-conflicts.md)

- [Déconnexion et reconnexion du recordset](disconnecting-and-reconnecting-the-recordset.md)

- [Mise à jour des résultats d'une opération JOIN  : Unique Table](updating-joined-results-unique-table.md)

