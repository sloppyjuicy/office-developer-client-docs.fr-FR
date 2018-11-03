---
title: Mode de traitement par lots (référence de base de données du bureau Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945788"
---
# <a name="batch-mode"></a>Mode de traitement par lots

**S’applique à**: Access 2013, Office 2013

Le mode de mise à jour par lot est utilisé lorsque la propriété **LockType** a la valeur **adLockBatchOptimistic** et que la mise à jour par lot est prise en charge par le fournisseur. Certains paramètres de verrouillage ne sont pas disponibles en fonction de l'emplacement du curseur. Par exemple, un type de verrouillage pessimiste n'est pas disponible lorsque **CursorLocation** a la valeur **adUseClient**. À l'inverse, il se peut qu'un fournisseur ne prenne pas en charge un verrouillage optimiste du traitement par lot lorsque le curseur est positionné sur le serveur. Vous devez utiliser la mise à jour par lot uniquement avec un jeu de clés ou un curseur statique.

La méthode **UpdateBatch** est utilisée pour envoyer les modifications de l'objet **Recordset** contenues dans le tampon de copie au serveur, afin de mettre à jour la source de données. La section suivante illustre l'ouverture d'un objet **Recordset** en mode de mise à jour par lot, la modification du tampon de copie puis l'envoi des modifications à la source de données par un appel à la méthode **UpdateBatch**.

Cette section comprend les rubriques suivantes :

- [Envoyer les mises à jour : UpdateBatch](sending-the-updates-updatebatch.md)
- [Filtrage des enregistrements mis à jour](filtering-for-updated-records.md)
- [Gérer les mises à jour échouées](dealing-with-failed-updates.md)
- [Détection et résolution des conflits](detecting-and-resolving-conflicts.md)
- [Déconnexion et reconnexion de l’objet Recordset](disconnecting-and-reconnecting-the-recordset.md)
- [Mise à jour des résultats de la jonction : Unique Table](updating-joined-results-unique-table.md)

