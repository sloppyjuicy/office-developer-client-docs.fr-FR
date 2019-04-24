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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="b7526-102">Octroi de privilèges invité à un ordinateur serveur Web; Privilèges des invités RDS</span><span class="sxs-lookup"><span data-stu-id="b7526-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="b7526-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7526-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7526-104">Le compte de serveur Web anonyme (\_IUSR*nomordinateur*) doit être ajouté au groupe local invités sur l'ordinateur serveur Web pour pouvoir utiliser RDS.</span><span class="sxs-lookup"><span data-stu-id="b7526-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="b7526-105">**Pour accorder des privilèges invité à un ordinateur serveur Web**</span><span class="sxs-lookup"><span data-stu-id="b7526-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="b7526-106">Sur votre ordinateur serveur Microsoft Windows 2000, cliquez sur **Démarrer**, pointez sur **programmes**, sur **Outils d'administration**, puis cliquez sur gestion de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="b7526-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="b7526-107">Dans l'arborescence de la console, dans **Utilisateurs et groupes locaux**, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b7526-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="b7526-p101">Sélectionnez le groupe local **Invités**. Dans le menu **Action**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b7526-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="b7526-110">Dans la boîte de dialogue **Propriétés de Invités**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b7526-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="b7526-111">Si le compte de serveur Web anonyme n'apparaît pas dans la liste de la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** , tapez\_son nom (IUSR*nomordinateur*) dans la zone de texte du bas, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b7526-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="b7526-112">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7526-112">Click **OK**.</span></span>

