---
title: Scénario de persistance des objets Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bbb8a3aa50027be7ce025a04d5987a45fee888f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471942"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="2ade8-102">Scénario de persistance des objets Recordset XML</span><span class="sxs-lookup"><span data-stu-id="2ade8-102">XML Recordset Persistence Scenario</span></span>


<span data-ttu-id="2ade8-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ade8-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="2ade8-104">Scénario de persistance des objets Recordset XML</span><span class="sxs-lookup"><span data-stu-id="2ade8-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="2ade8-105">Ce scénario consiste à créer une application ASP (Active Server Pages) enregistrant directement le contenu d'un objet **Recordset** dans l'objet **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="2ade8-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2ade8-106">[!REMARQUE] Pour les besoins de ce scénario, Internet Information Server 5.0 (IIS) ou une version ultérieure doit être installé sur votre serveur.</span><span class="sxs-lookup"><span data-stu-id="2ade8-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span></P>



<span data-ttu-id="2ade8-107">L'objet **Recordset** retourné est affiché dans Internet Explorer à l'aide d'un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="2ade8-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="2ade8-108">Pour créer ce scénario, il est nécessaire d'exécuter les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ade8-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="2ade8-109">Configurer l'application</span><span class="sxs-lookup"><span data-stu-id="2ade8-109">Set up the application.</span></span>

2.  <span data-ttu-id="2ade8-110">Obtenir les données</span><span class="sxs-lookup"><span data-stu-id="2ade8-110">Get the data.</span></span>

3.  <span data-ttu-id="2ade8-111">Envoyer les données</span><span class="sxs-lookup"><span data-stu-id="2ade8-111">Send the data.</span></span>

4.  <span data-ttu-id="2ade8-112">Recevoir et afficher les données</span><span class="sxs-lookup"><span data-stu-id="2ade8-112">Receive and display the data.</span></span>

<span data-ttu-id="2ade8-113">**Suite**[Étape 1 : configurer l'application](step-1-set-up-the-application.md)</span><span class="sxs-lookup"><span data-stu-id="2ade8-113">**Next**[Step 1: Set Up the Application](step-1-set-up-the-application.md)</span></span>

