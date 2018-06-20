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
# <a name="about-the-infopath-xml-interop-assembly"></a>À propos de l’assembly d’interopérabilité XML InfoPath

L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge pour l’interopérabilité entre le code managé et le serveur COM exposés par Microsoft XML Core Services (MSXML) à partir d’applications externes qui automatisent InfoPath.

L’option de **Prise en charge de la programmabilité .NET** dans le programme d’installation de InfoPath installe trois assemblys d’interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. Une de ces assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, fournit les membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , qui est utilisée pour travailler avec les membres exposés par le serveur COM pour Microsoft XML Core Services (MSXML) à partir d’applications externes qui automatisent InfoPath à l’aide de code managé. 
  
> [!NOTE]
> Les références aux assemblys PIA Microsoft.Office.Interop.InfoPath.dll et Microsoft.Office.Interop.InfoPath.Xml.dll qui sont requis pour les projets d’automatisation externe InfoPath doivent être établies manuellement. Pour plus d’informations sur l’automatisation externe, voir [scénarios d’automatisation externe et des exemples](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

