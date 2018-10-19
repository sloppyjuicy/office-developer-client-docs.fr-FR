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
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="17e37-102">Modification de la présentation d’une carte de visite électronique</span><span class="sxs-lookup"><span data-stu-id="17e37-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="17e37-103">Cet exemple montre comment modifier la présentation d’une carte de visite électronique à l’aide de la propriété [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de l’interface [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="17e37-103">This example shows how to modify the layout of an Electronic Business Card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="17e37-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="17e37-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="17e37-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="17e37-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="17e37-106">Une carte de visite électronique propose un affichage contenant des informations spécifiques sur un contact.</span><span class="sxs-lookup"><span data-stu-id="17e37-106">An Electronic Business Card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="17e37-107">L’interface **ContactItem** fournit des membres spécifiques pour les cartes de visite électroniques.</span><span class="sxs-lookup"><span data-stu-id="17e37-107">The **ContactItem** interface provides specific members that pertain to Electronic Business Cards.</span></span> <span data-ttu-id="17e37-108">Ces membres sont **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) et [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="17e37-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)) , [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)) , [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)) , [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)) , [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) , and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)) .</span></span>

<span data-ttu-id="17e37-109">Dans l’exemple de code suivant, BusinessCardLayoutExample modifie la présentation d’une carte de visite électronique en commençant par obtenir un objet **ContactItem** spécifique.</span><span class="sxs-lookup"><span data-stu-id="17e37-109">In the following code example,   modifies the layout of an Electronic Business Card by first obtaining a specified ContactItem object.</span></span> <span data-ttu-id="17e37-110">Dans le cas présent, l’objet **ContactItem** est un contact dont la valeur de la propriété [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) est égale à « Melissa MacBeth ».</span><span class="sxs-lookup"><span data-stu-id="17e37-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to "Melissa MacBeth".</span></span> <span data-ttu-id="17e37-111">Ensuite, BusinessCardLayoutExample crée une classe de documents [XmlDocument](https://msdn.microsoft.com/fr-FR/library/6kza7w4k), puis obtient l’attribut de présentation de cette classe dans une chaîne en utilisant la valeur **BusinessCardLayoutXML** de l’objet **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="17e37-111">Next,   creates an XML document class XmlDocument , and then gets the layout attribute of this class in a string by using the BusinessCardLayoutXML value for the ContactItem object.</span></span> <span data-ttu-id="17e37-112">La présentation de la carte passe ensuite de aligné à gauche à aligné à droite.</span><span class="sxs-lookup"><span data-stu-id="17e37-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="17e37-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="17e37-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="17e37-114">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="17e37-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="17e37-115">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="17e37-115">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="17e37-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17e37-116">See also</span></span>

- [<span data-ttu-id="17e37-117">Cartes de visite électroniques</span><span class="sxs-lookup"><span data-stu-id="17e37-117">Electronic Business Cards</span></span>](electronic-business-cards.md)

