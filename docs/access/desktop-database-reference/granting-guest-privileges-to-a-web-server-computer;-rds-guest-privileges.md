---
title: Octroi de privilèges invité à un serveur Web ; Privilèges invité de RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed450913c7512e8ef20983484ca4b874878fd791
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867166"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Octroi de privilèges invité à un serveur Web ; Privilèges invité de RDS 


**S’applique à**: Access 2013, Office 2013

Le compte de serveur web anonyme (IUSR\_*ComputerName*) doit être ajouté au groupe local invités sur l’ordinateur serveur web à utiliser RDS.

**Pour accorder des privilèges invité à un serveur Web**

1.  Sur votre ordinateur Microsoft Windows® 2000 Server, cliquez sur **Démarrer**, pointez sur **Programmes**, sur **Outils d'administration** puis cliquez sur **Gestion de l'ordinateur**.

2.  Dans l'arborescence de la console, dans **Utilisateurs et groupes locaux**, cliquez sur **Groupes**.

3.  Sélectionnez le groupe local **Invités**. Dans le menu **Action**, choisissez **Propriétés**.

4.  Dans la boîte de dialogue **Propriétés de Invités**, cliquez sur **Ajouter**.

5.  Si le compte de serveur web anonyme n’apparaît pas dans la liste dans la boîte de dialogue **Sélectionner des utilisateurs ou groupes** , tapez son nom (IUSR\_*ComputerName*) vers le bas vide zone, puis cliquez sur **Ajouter**.

6.  Cliquez sur **OK**.

