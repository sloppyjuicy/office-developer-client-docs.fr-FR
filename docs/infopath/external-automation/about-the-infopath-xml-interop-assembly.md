---
title: À propos de l’assembly InfoPath XML Interop
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007],InfoPath 2007, assembly d’interopérabilité principale XML, assembly d’interopérabilité XML InfoPath
ms.localizationpriority: medium
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge de l’interopérabilité entre le code managé et le serveur COM exposé par Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath.
ms.openlocfilehash: 9c175cea8f9133f9d3b30628e0186656a9aa1b5b
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770998"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>À propos de l’assembly InfoPath XML Interop

L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge de l’interopérabilité entre le code managé et le serveur COM exposé par Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath.

L’option **prise en charge de la programmabilité .NET** dans le programme d’installation d’InfoPath installe trois assemblys d’interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. L’un de ces assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, fournit les membres de [ l’espace ](/dotnet/api/microsoft.office.interop.infopath.xml) de nomsMicrosoft.Office.Interop.InfoPath.Xml, qui est utilisé pour travailler avec les membres exposés par le serveur COM pour Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath à l’aide de code managé. 
  
> [!NOTE]
> Les références aux assemblys d’interopérabilité Microsoft.Office.Interop.InfoPath.dll et Microsoft.Office.Interop.InfoPath.Xml.dll requis pour les projets d’automatisation externe InfoPath doivent être établies manuellement. Pour plus d’informations sur l’automatisation externe, consultez [Scénarios et exemples d’automatisation externe](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

