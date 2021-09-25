---
title: Modification de la présentation d’une carte de visite électronique
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-modify-the-layout-of-an-electronic-business-card?redirectedfrom=MSDN
ms:contentKeyID: 55119838
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b94119b0625793a2eac80c2ae58a924fb8ed3c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574642"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modification de la présentation d’une carte de visite électronique

Cet exemple montre comment modifier la présentation d’une carte de visite électronique à l’aide de la propriété [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de l’interface [ContactItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.contactitem?redirectedfrom=MSDN&view=outlook-pia).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Une carte de visite électronique propose un affichage contenant des informations spécifiques sur un contact. L’interface **ContactItem** fournit des membres spécifiques pour les cartes de visite électroniques. Ces membres sont **BusinessCardLayoutXml**, [BusinessCardType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.businesscardtype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_BusinessCardType), [AddBusinessCardLogoPicture(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.addbusinesscardlogopicture?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_AddBusinessCardLogoPicture_System_String_), [ForwardAsBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.forwardasbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ForwardAsBusinessCard), [ResetBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.resetbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ResetBusinessCard), [SaveBusinessCardImage(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.savebusinesscardimage?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_SaveBusinessCardImage_System_String_) et [ShowBusinessCardEditor()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.showbusinesscardeditor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ShowBusinessCardEditor).

Dans l’exemple de code suivant, BusinessCardLayoutExample modifie la présentation d’une carte de visite électronique en commençant par obtenir un objet **ContactItem** spécifique. Dans le cas présent, l’objet **ContactItem** est un contact dont la valeur de la propriété [Subject](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.subject?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_Subject) est égale à « Melissa MacBeth ». Ensuite, BusinessCardLayoutExample crée une classe de documents [XmlDocument](https://msdn.microsoft.com/library/6kza7w4k), puis obtient l’attribut de présentation de cette classe dans une chaîne en utilisant la valeur **BusinessCardLayoutXML** de l’objet **ContactItem**. La présentation de la carte passe ensuite de aligné à gauche à aligné à droite.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

