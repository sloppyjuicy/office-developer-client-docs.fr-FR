---
title: Modification de la présentation d’une carte de visite électronique
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0b95621df2e021f52587d5a40d0de43e5505b80c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406434"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modification de la présentation d’une carte de visite électronique

Cet exemple montre comment modifier la présentation d’une carte de visite électronique à l’aide de la propriété [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de l’interface [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Une carte de visite électronique propose un affichage contenant des informations spécifiques sur un contact. L’interface **ContactItem** fournit des membres spécifiques pour les cartes de visite électroniques. Ces membres sont **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) et [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).

Dans l’exemple de code suivant, BusinessCardLayoutExample modifie la présentation d’une carte de visite électronique en commençant par obtenir un objet **ContactItem** spécifique. Dans le cas présent, l’objet **ContactItem** est un contact dont la valeur de la propriété [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) est égale à « Melissa MacBeth ». Ensuite, BusinessCardLayoutExample crée une classe de documents [XmlDocument](https://msdn.microsoft.com/fr-FR/library/6kza7w4k), puis obtient l’attribut de présentation de cette classe dans une chaîne en utilisant la valeur **BusinessCardLayoutXML** de l’objet **ContactItem**. La présentation de la carte passe ensuite de aligné à gauche à aligné à droite.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

