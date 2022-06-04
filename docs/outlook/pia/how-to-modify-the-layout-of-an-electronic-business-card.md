---
title: Modification de la présentation d’une carte de visite électronique
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-modify-the-layout-of-an-electronic-business-card?redirectedfrom=MSDN
ms:contentKeyID: 55119838
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a22a1b79b45be7ee17a156eff7de343500df64e6
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894375"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modification de la présentation d’une carte de visite électronique

Cet exemple montre comment modifier la présentation d’une carte de visite électronique à l’aide de la propriété [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de l’interface [ContactItem](/dotnet/api/microsoft.office.interop.outlook.contactitem).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Une carte de visite électronique propose un affichage contenant des informations spécifiques sur un contact. L’interface **ContactItem** fournit des membres spécifiques pour les cartes de visite électroniques. Ces membres sont **BusinessCardLayoutXml**, [BusinessCardType](/dotnet/api/microsoft.office.interop.outlook._contactitem.businesscardtype), [AddBusinessCardLogoPicture(String)](/dotnet/api/microsoft.office.interop.outlook._contactitem.addbusinesscardlogopicture), [ForwardAsBusinessCard()](/dotnet/api/microsoft.office.interop.outlook._contactitem.forwardasbusinesscard), [ResetBusinessCard()](/dotnet/api/microsoft.office.interop.outlook._contactitem.resetbusinesscard), [SaveBusinessCardImage(String)](/dotnet/api/microsoft.office.interop.outlook._contactitem.savebusinesscardimage) et [ShowBusinessCardEditor()](/dotnet/api/microsoft.office.interop.outlook._contactitem.showbusinesscardeditor).

Dans l’exemple de code suivant, BusinessCardLayoutExample modifie la présentation d’une carte de visite électronique en commençant par obtenir un objet **ContactItem** spécifique. Dans le cas présent, l’objet **ContactItem** est un contact dont la valeur de la propriété [Subject](/dotnet/api/microsoft.office.interop.outlook._contactitem.subject) est égale à « Melissa MacBeth ». Ensuite, BusinessCardLayoutExample crée une classe de documents [XmlDocument](https://msdn.microsoft.com/library/6kza7w4k), puis obtient l’attribut de présentation de cette classe dans une chaîne en utilisant la valeur **BusinessCardLayoutXML** de l’objet **ContactItem**. La présentation de la carte passe ensuite de aligné à gauche à aligné à droite.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration Class publique. La ligne de code suivante montre comment effectuer l’importation et l’affectation dans C \#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Cartes de visite électroniques](electronic-business-cards.md)

