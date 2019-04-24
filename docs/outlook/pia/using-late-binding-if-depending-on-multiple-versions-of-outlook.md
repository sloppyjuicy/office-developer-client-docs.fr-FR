---
title: Utilisation de la liaison tardive en cas de dépendance envers plusieurs versions d’Outlook
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4cca4d426e5e7e9fd06fa3a0c3af1158b7e6c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357469"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>Utilisation de la liaison tardive en cas de dépendance envers plusieurs versions d’Outlook

Les compléments Outlook gérés qui utilisent l’assembly PIA Outlook sont compilés avec les informations de type fournies par l’assembly PIA. Cette **liaison anticipée** des informations de type pour les méthodes et propriétés permet au compilateur d’effectuer des contrôles de syntaxe et de type afin de s’assurer que la quantité correcte et le type correct de paramètres sont passés à la méthode ou à la propriété, et que la valeur renvoyée est du type attendu. 

Cependant, la liaison anticipée présente l'inconvénient d'introduire une incompatibilité de version si une méthode ou propriété appelée par le complément a une déclaration différente dans une version antérieure. Par exemple, l'ajout de nouvelles méthodes et propriétés ou la modification de membres existants d'un objet peut entraîner une modification de la disposition binaire de l'objet et provoquer des problèmes avec un complément managé qui utilise les informations de type plus récentes pour automatiser une version antérieure d'Outlook. 

Dans ces cas-là, la **liaison tardive** attend l’exécution pour lier les appels de propriété et de méthode à leurs objets. La liaison tardive peut aider à éviter les complications liées aux types qui diffèrent dans différentes versions d'Outlook, et est particulièrement utile lors de l'écriture de compléments qui dépendent de plusieurs versions d'Outlook.

La liaison tardive implique qu’un complément appelle l’interface [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) implémentée par Outlook. Pour utiliser la liaison tardive en Visual C\#, utilisez la méthode [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2). Cette méthode appelle [IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) pour établir une liaison aux méthodes et propriétés d’Outlook. La méthode IDispatch::GetIDsOfNames permet à Visual C\# d’interroger un objet afin de déterminer les méthodes et propriétés qu’il prend en charge et la méthode IDispatch::Invoke permet ensuite à Visual C\# d’appeler ces méthodes et propriétés. 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>Voir aussi

- [Introduction à l’interopérabilité entre COM et .NET](introduction-to-interoperability-between-com-and-net.md)

