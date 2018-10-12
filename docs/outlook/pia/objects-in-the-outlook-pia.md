---
title: Objets dans l’assembly PIA Outlook
TOCTitle: Objects in the Outlook PIA
ms:assetid: 1be732a6-d6da-4fa0-beaa-accf35db12d6
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609459(v=office.15)
ms:contentKeyID: 55119778
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 434be5dc9193beaf9723530c6d963ed0a96d8884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407029"
---
# <a name="objects-in-the-outlook-pia"></a>Objets dans l’assembly PIA Outlook

Lors de l'exploration de l'assembly PIA (Primary Interop Assembly) Outlook dans un explorateur d'objets, vous pouvez remarquer que de nombreuses interfaces et classes ont des noms qui font référence à des objets familiers dans le modèle objet Outlook. Certains objets du modèle objet ont un mappage un-à-un à des interfaces dans l'assembly PIA. 

Par exemple, **AddressEntry** est mappé à l'interface [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) et l'objet **AddressList** est mappé à l'interface [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) dans l'assembly PIA. 

Cependant, la plupart des autres objets ont un mappage un-à-plusieurs dans l'assembly PIA. Ce mappage un-à-plusieurs s'applique à certains objets qui existaient avant Microsoft Office Outlook 2007, et à tous les objets ajoutés depuis Outlook 2007. Cette rubrique répertorie les interfaces, classes et délégués .NET par défaut qui sont mappés à un objet COM et décrit comment accéder à un objet dans l'assembly PIA Outlook. Elle décrit également quelques exceptions dans l’assembly PIA Outlook où les objets sont masqués ou obsolètes dans le modèle objet COM.

## <a name="helper-objects"></a>Objets d’assistance

Cette section illustre les classes d'assistance par défaut pour un objet dans l'assembly PIA Outlook en utilisant l'objet **FormRegion** en guise d'exemple. L'objet **FormRegion** a été ajouté au modèle objet dans Outlook 2007. Les interfaces, classes et délégués illustrés à la Figure 1 sont liés à l'objet **FormRegion** dans l'assembly PIA.

**Figure 1. Objet FormRegion représenté dans le modèle objet Outlook et dans l’assembly PIA Outlook**

![Objet FormRegion représenté dans le modèle objet Outlook et dans l’assembly PIA Outlook](media/pia-outlook-object-model.gif)

L'interface que l'on utilise le plus pour accéder à l'objet **FormRegion** et à ses méthodes, propriétés et membres d'événements est l'interface [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) . Toutefois, il ne faut pas considérer l’interface .NET **FormRegion** comme le miroir exact de l’objet COM **FormRegion**. Si vous observez l’Explorateur d’objets dans Visual Studio, vous remarquerez que l’interface **FormRegion** hérite d’une autre interface, l’interface [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)). En fait, l'interface **FormRegion** est simplement l'une des quelques interfaces et classes qui résultent de la création de l'assembly PIA Outlook sur la base de la bibliothèque de types COM.

Pour créer l'assembly PIA Outlook, Outlook utilise l'importateur de bibliothèques de types (TLBIMP) dans le .NET Framework pour convertir les définitions de types dans la bibliothèque de types COM en définitions équivalentes dans un assembly CLR (Common Language Runtime). Dans COM, l'objet **FormRegion** est en fait une coclasse constituée des deux interfaces suivantes définissant les interfaces implémentées par l'objet **FormRegion**:

- l’interface principale **\_FormRegion** ;

- l’interface d’événement [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\)).

TLBIMP importe directement **\_FormRegion** et **FormRegionEvents** à partir de la bibliothèque de types.

En plus d'importer l'interface principale et l'interface d'événement, TLBIMP crée une interface .NET portant le même nom que l'objet COM et une classe .NET qui utilise le nom de l'objet et y ajoute le terme « Class ». Dans le cas de l'objet **FormRegion**, TLBIMP crée les éléments suivants :

- l'interface .NET **FormRegion**;

- la classe .NET [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)) .

Parmi les interfaces.NET et les classes .NET mentionnées dans cette rubrique, il convient de toujours utiliser l'interface .NET créée par TLBIMP pour accéder à un objet. Par exemple, pour accéder à un objet **FormRegion** en VB, on utilise toujours l'interface **FormRegion**, comme dans l'exemple de code suivant :

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
Sub DemoFormRegion(ByVal Region As Outlook.FormRegion)
    Dim MyFormRegion As Outlook.FormRegion = Region
    ' Additional method code here
End Sub
```

<br/>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook; 
void DemoFormRegion(Outlook.FormRegion region) 
{
    Outlook.FormRegion myFormRegion = region; 
    // Additional method code here
}
```

Pour plus d’informations sur le rôle de l’interface principale et de la classe .NET importées et créées par TLBIMP, reportez-vous à la rubrique [Méthodes et propriétés dans l’assembly PIA Outlook](methods-and-properties-in-the-outlook-pia.md). Pour plus d’informations sur l’objectif des interfaces liées aux événements, les délégués et les récepteurs des classes d’assistance, reportez-vous à l’article relatif aux [événements dans l’assembly PIA Outlook](events-in-the-outlook-pia.md).

## <a name="deprecated-objects"></a>Objets obsolètes

Les objets obsolètes dans la bibliothèque de types sont exposés dans l’assembly PIA Outlook. Par exemple, les objets **\_DDocSiteControl** et **\_DRecipientControl** sont masqués dans la bibliothèque de types, mais sont exposés dans l’assembly PIA.

Un autre exemple d’objet obsolète est l’objet **MAPIFolder**. À compter de Outlook 2007, l'objet **Folder** remplace l'objet **MAPIFolder** dans le modèle objet. Les solutions existantes doivent remplacer les références à **MAPIFolder** par **Folder**, et toutes les nouvelles solutions pour Outlook 2007 et versions ultérieures doivent utiliser uniquement l'objet **Folder**. Pour les solutions non managées, l'Explorateur d'objets de Visual Basic Editor ne mentionne plus l'objet **MAPIFolder**, pas même sous forme masquée. 

Pour les solutions managées, bien que l'assembly PIA Outlook expose une interface [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) par le biais de laquelle vous accédez à l'objet **Folder** et à ses membres, l'assembly Outlook expose également [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) en tant qu'interface qui définit les membres de l'objet **Folder**.

## <a name="see-also"></a>Voir aussi

- [Mise en rapport de l’assembly PIA Outlook avec le modèle objet](relating-the-outlook-pia-with-the-object-model.md)


