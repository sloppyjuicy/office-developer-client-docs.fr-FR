---
title: À propos de l’assembly d’interopérabilité XML InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- MSXML interop [infopath 2007], InfoPath 2007, assembly PIA XML, l’assembly d’interopérabilité XML InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge pour l’interopérabilité entre le code managé et le serveur COM exposés par Microsoft XML Core Services (MSXML) à partir d’applications externes qui automatisent InfoPath.
ms.openlocfilehash: 8d3fb1c1de141fe23c655e82b77d83a8e2b11abd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782237"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="ffba3-104">À propos de l’assembly d’interopérabilité XML InfoPath</span><span class="sxs-lookup"><span data-stu-id="ffba3-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="ffba3-105">L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge pour l’interopérabilité entre le code managé et le serveur COM exposés par Microsoft XML Core Services (MSXML) à partir d’applications externes qui automatisent InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ffba3-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="ffba3-106">L’option de **Prise en charge de la programmabilité .NET** dans le programme d’installation de InfoPath installe trois assemblys d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="ffba3-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="ffba3-107">Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents.</span><span class="sxs-lookup"><span data-stu-id="ffba3-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="ffba3-108">Une de ces assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, fournit les membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , qui est utilisée pour travailler avec les membres exposés par le serveur COM pour Microsoft XML Core Services (MSXML) à partir d’applications externes qui automatisent InfoPath à l’aide de code managé.</span><span class="sxs-lookup"><span data-stu-id="ffba3-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ffba3-109">Les références aux assemblys PIA Microsoft.Office.Interop.InfoPath.dll et Microsoft.Office.Interop.InfoPath.Xml.dll qui sont requis pour les projets d’automatisation externe InfoPath doivent être établies manuellement.</span><span class="sxs-lookup"><span data-stu-id="ffba3-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="ffba3-110">Pour plus d’informations sur l’automatisation externe, voir [scénarios d’automatisation externe et des exemples](external-automation-scenarios-and-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ffba3-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffba3-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffba3-111">See also</span></span>

- [<span data-ttu-id="ffba3-112">Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="ffba3-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

