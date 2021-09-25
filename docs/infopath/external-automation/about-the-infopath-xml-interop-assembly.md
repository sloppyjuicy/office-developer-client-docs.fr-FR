---
title: À propos de l’assembly d’opation XML InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007],InfoPath 2007, XML primary interop assembly,InfoPath XML interop assembly
ms.localizationpriority: medium
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge de l’interopérabilité entre le code géré et le serveur COM exposé par Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath.
ms.openlocfilehash: bae183892569652a41e62b302518fb43b933a370
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572346"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>À propos de l’assembly d’opation XML InfoPath

L’assembly d’interopérabilité XML InfoPath est fourni pour permettre la prise en charge de l’interopérabilité entre le code géré et le serveur COM exposé par Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath.

L’option Prise en charge **de la programmabilité .NET** dans le programme d’installation d’InfoPath installe trois assemblys d’interop. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. L’un de ces assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, fournit les membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml,](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) qui est utilisé pour travailler avec les membres exposés par le serveur COM pour Microsoft XML Core Services® (MSXML) à partir d’applications externes qui automatisent InfoPath à l’aide de code géré. 
  
> [!NOTE]
> Les références aux assemblys Microsoft.Office.Interop.InfoPath.dll et Microsoft.Office.Interop.InfoPath.Xml.dll d’interopation requises pour les projets d’automatisation externe InfoPath doivent être établies manuellement. Pour plus d’informations sur l’automatisation externe, voir [Scénarios et exemples d’automatisation externe.](external-automation-scenarios-and-examples.md) 
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

