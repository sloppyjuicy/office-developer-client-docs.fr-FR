---
title: Utilisation d’un domaine d’application distinct pour éviter les blocages
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b397fa2ad37102e12a3a0cf569e74323391b8e86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407253"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a>Utilisation d’un domaine d’application distinct pour éviter les blocages

Les compléments managés qui implémentent l'interface **IDTExtensibility2** sont chargés dans le même domaine d'application par défaut. En cas d'échec d'un complément dans le domaine d'application, les autres compléments de ce même domaine échouent également.

Pour contourner ce problème, vous pouvez créer un shim pour le complément de sorte que ce dernier puisse être chargé dans son propre domaine d'application. Un shim est une bibliothèque de liens dynamiques non managés écrite en C++. Lorsque vous utilisez un shim, vous enregistrez le shim à la place du complément. Outlook charge le shim et le shim charge le complément pour lequel il a été créé. Vous devez créer et enregistrer un shim distinct pour chaque complément. Pour plus d'informations sur le développement de shims pour les compléments managés, voir [Isolation des extensions Office avec l'Assistant Shim COM (éventuellement en anglais)](https://go.microsoft.com/fwlink/?linkid=89109).

Une autre solution pour charger votre complément dans un domaine d’application distinct est de développer votre complément à l’aide des Outils de développement Office dans Visual Studio 2010 ou une version ultérieure des Outils de développement Office pour Visual Studio. Les compléments développés par ces versions des Outils de développement Office pour Visual Studio n’implémentent pas l’interface IDTExtensibility2, mais utilisent l’interface **IStartup**. Ils utilisent un chargeur fourni par Visual Studio, AddinLoader.dll, qui agit comme un shim générique. Outlook recherche dans le Registre les compléments créés avec Visual Studio. 

Si Outlook trouve ce type de compléments, Outlook lance AddinLoader.dll, qui lance ensuite Visual Studio Tools pour Office Runtime pour lui transmettre le manifeste d’application. Visual Studio Tools pour Office Runtime charge ensuite chacun de ces compléments dans un domaine d’application distinct. Pour savoir comment Visual Studio charge un complément, consultez l’article relatif à l’[architecture des compléments d’application](https://msdn.microsoft.com/library/bb386298\(v=office.15\)).

