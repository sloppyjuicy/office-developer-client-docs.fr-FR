---
title: Octroi de privilèges invité à un ordinateur serveur Web; Privilèges des invités RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292124"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Octroi de privilèges invité à un ordinateur serveur Web; Privilèges des invités RDS

**S’applique à** : Access 2013, Office 2013

Le compte de serveur Web anonyme (\_IUSR*nomordinateur*) doit être ajouté au groupe local invités sur l'ordinateur serveur Web pour pouvoir utiliser RDS.

**Pour accorder des privilèges invité à un ordinateur serveur Web**

1.  Sur votre ordinateur serveur Microsoft Windows 2000, cliquez sur **Démarrer**, pointez sur **programmes**, sur **Outils d'administration**, puis cliquez sur gestion de l' **ordinateur**.

2.  Dans l'arborescence de la console, dans **Utilisateurs et groupes locaux**, cliquez sur **Groupes**.

3.  Sélectionnez le groupe local **Invités**. Dans le menu **Action**, choisissez **Propriétés**.

4.  Dans la boîte de dialogue **Propriétés de Invités**, cliquez sur **Ajouter**.

5.  Si le compte de serveur Web anonyme n'apparaît pas dans la liste de la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** , tapez\_son nom (IUSR*nomordinateur*) dans la zone de texte du bas, puis cliquez sur **Ajouter**.

6.  Cliquez sur **OK**.

