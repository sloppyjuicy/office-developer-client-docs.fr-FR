---
title: À propos de l'assembly XML InfoPath Interop
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- interopérabilité MSXML [InfoPath 2007], InfoPath 2007, XML Primary Interop Assembly, assembly XML InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: L'assembly d'interopérabilité XML d'InfoPath est fourni pour permettre la prise en charge de l'interopérabilité entre le code managé et le serveur COM exposé par MSXML (Microsoft XML Core Services) à partir d'applications externes qui automatisent InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303779"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>À propos de l'assembly XML InfoPath Interop

L'assembly d'interopérabilité XML d'InfoPath est fourni pour permettre la prise en charge de l'interopérabilité entre le code managé et le serveur COM exposé par MSXML (Microsoft XML Core Services) à partir d'applications externes qui automatisent InfoPath.

L'option **prise en charge** de la programmabilité .net dans le programme d'installation d'InfoPath installe trois assemblys d'interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. L'un de ces assemblys, Microsoft. Office. Interop. InfoPath. Xml. dll, fournit les membres de l'espace de noms [Microsoft. Office. Interop. InfoPath. xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) , qui est utilisé pour utiliser des membres exposés par le serveur com pour Microsoft XML Core Services (MSXML) à partir d'applications externes qui automatisent InfoPath à l'aide de code managé. 
  
> [!NOTE]
> Les références aux assemblys d'interopérabilité Microsoft. Office. Interop. InfoPath. dll et Microsoft. Office. Interop. InfoPath. Xml. dll requises pour les projets d'automatisation externe InfoPath doivent être établies manuellement. Pour plus d'informations sur l'automatisation externe, consultez la rubrique [scénarios d'automatisation externe et exemples](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

