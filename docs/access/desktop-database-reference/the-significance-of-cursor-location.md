---
title: Importance de l'emplacement du curseur
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1b552ac2774fe0c5d47c19924219800e5bdf865
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469951"
---
# <a name="the-significance-of-cursor-location"></a>Importance de l'emplacement du curseur


**S’applique à**: Access 2013 | Office 2013

Chaque curseur utilise des ressources temporaires pour contenir ses données. Ces ressources peuvent correspondre à la mémoire, à un fichier de pagination disque, à des fichiers disque temporaires ou même à un stockage temporaire dans la base de données. Le curseur est appelé un curseur *côté client* lorsque ces ressources sont hébergées sur l’ordinateur client. Le curseur est appelé un curseur *côté serveur* lorsque ces ressources sont situés sur le serveur.

## <a name="client-side-cursors"></a>Curseurs côté client

Dans ADO, appelez un curseur côté client en utilisant la valeur **adUseClient** pour **CursorLocationEnum**. Avec un curseur côté client autre qu'un jeu de clés, le serveur envoie le jeu complet de résultats via le réseau à l'ordinateur client. L'ordinateur client fournit et gère les ressources temporaires requises par le curseur et le jeu de résultats. L'application cliente peut parcourir tout le jeu de résultats pour déterminer les lignes requises.

Les curseurs côté client statiques et pilotés par des jeux de clés, peuvent induire une charge importante pour votre station de travail s'ils comprennent trop de lignes. Contrairement à toutes les bibliothèques de curseurs conçues pour créer des curseurs dotés de milliers de lignes, les applications destinées à l'extraction de tels jeux de lignes risquent de présenter des performances médiocres. Bien entendu, il y a des exceptions à la règle. Pour certaines applications, un curseur côté client volumineux peut être tout à fait approprié sans que les performances posent de soucis.

Le curseur côté client a pour principal avantage d'être rapide. Après le téléchargement du jeu de résultats vers l'ordinateur client, la navigation des lignes est extrêmement rapide. En général, votre application s'adapte plus facilement aux curseurs côté client car les ressources requises par le curseur s'appliquent à chaque client et non au serveur.

## <a name="server-side-cursors"></a>Curseurs côté serveur

Dans ADO, appelez un curseur côté serveur en utilisant la valeur **adUseServer** pour **CursorLocationEnum.** Avec un curseur côté serveur, le serveur gère le jeu de résultats en utilisant les ressources fournies par l'ordinateur serveur. Le curseur côté serveur retourne uniquement les données demandées sur le réseau. Ce type de curseur peut parfois offrir de meilleures performances que le curseur côté client, notamment dans le cas où un trafic réseau élevé pose un problème.

Cependant, il est important de signaler qu'un curseur côté serveur consomme  temporairement, du moins  d'importantes ressources du serveur pour chaque client actif. Veillez à planifier les ressources en conséquence afin que le matériel serveur soit en mesure de gérer tous les curseurs côté serveur demandés par des clients actifs. En outre, un curseur côté serveur peut être lent car il fournit uniquement un accès ligne par ligne  aucun curseur d'accès par lot n'est disponible.

Les curseurs côté serveur sont pratiques pour l'insertion, la mise à jour ou la suppression d'enregistrements. Avec des curseurs côté serveur, vous pouvez avoir plusieurs instructions actives sur la même connexion.

