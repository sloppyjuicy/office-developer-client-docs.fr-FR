---
title: Installation et référencement de l’assembly PIA Outlook
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718202"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="81e55-102">Installation et référencement de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="81e55-102">Installing and referencing the Outlook PIA</span></span>

<span data-ttu-id="81e55-103">Nous vous recommandons d’installer l’assembly PIA (Primary Interop Assembly) Outlook dans le cache GAC (Global Assembly Cache) avant d’incorporer les informations de l’assembly PIA dans un complément managé Outlook.</span><span class="sxs-lookup"><span data-stu-id="81e55-103">You must have the Outlook Primary Interop Assembly (PIA) installed in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in.</span></span> <span data-ttu-id="81e55-104">Par défaut, l’assembly PIA est installé automatiquement quand vous installez Office sur l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="81e55-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="81e55-105">Toutefois, pour installer l’assembly PIA séparément, consultez l’article [Configurer un ordinateur pour développer des solutions Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="81e55-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="81e55-106">Seule une personne ayant un rôle d’administrateur sur l’ordinateur de développement peut installer les assemblies PIA Office.</span><span class="sxs-lookup"><span data-stu-id="81e55-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="81e55-107">Après l’installation, si vous utilisez Visual Studio pour créer le projet managé, vous pouvez ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0.</span><span class="sxs-lookup"><span data-stu-id="81e55-107">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 15.0 Object Library component.</span></span> <span data-ttu-id="81e55-108">Par la suite, dans le navigateur d'objets, sous l'espace de noms **Microsoft.Office.Interop.Outlook**, vous pouvez voir les interfaces managées de l'assembly PIA dont les noms correspondent aux objets du modèle objet Outlook.</span><span class="sxs-lookup"><span data-stu-id="81e55-108">Subsequently, in the object browser, under the **Microsoft.Office.Interop.Outlook** namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="81e55-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81e55-109">See also</span></span>

- [<span data-ttu-id="81e55-110">Installation des assemblies PIA Office</span><span class="sxs-lookup"><span data-stu-id="81e55-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [<span data-ttu-id="81e55-111">Architecture de l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="81e55-111">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)

