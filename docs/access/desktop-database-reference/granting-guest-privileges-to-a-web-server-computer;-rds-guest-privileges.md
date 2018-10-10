---
title: Octroi de privilèges invité à un serveur Web ; Privilèges invité de RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d09de280c9edcfdf4305bb6c2ba09aa01e556ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471052"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="6ae62-102">Octroi de privilèges invité à un serveur Web ; Privilèges invité de RDS</span><span class="sxs-lookup"><span data-stu-id="6ae62-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="6ae62-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ae62-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ae62-104">Le compte de serveur Web anonyme (IUSR\_*ComputerName*) doit être ajouté au groupe local invités sur l’ordinateur serveur Web à utiliser RDS.</span><span class="sxs-lookup"><span data-stu-id="6ae62-104">The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<span data-ttu-id="6ae62-105">**Pour accorder des privilèges Invité à un serveur Web**</span><span class="sxs-lookup"><span data-stu-id="6ae62-105">**To grant guest privileges to a Web server computer**</span></span>

1.  <span data-ttu-id="6ae62-106">Sur votre ordinateur Microsoft Windows® 2000 Server, cliquez sur **Démarrer**, pointez sur **Programmes**, sur **Outils d'administration** puis cliquez sur **Gestion de l'ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="6ae62-107">Dans l'arborescence de la console, dans **Utilisateurs et groupes locaux**, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="6ae62-p101">Sélectionnez le groupe local **Invités**. Dans le menu **Action**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="6ae62-110">Dans la boîte de dialogue **Propriétés de Invités**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="6ae62-111">Si le compte de serveur Web anonyme n’apparaît pas dans la liste dans la boîte de dialogue **Sélectionner des utilisateurs ou groupes** , tapez son nom (IUSR\_*ComputerName*) vers le bas vide zone, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-111">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="6ae62-112">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ae62-112">Click **OK**.</span></span>

