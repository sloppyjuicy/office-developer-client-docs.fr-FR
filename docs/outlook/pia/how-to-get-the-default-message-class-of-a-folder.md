---
title: Obtention de la classe de message par défaut d’un dossier
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bef6ebe051e669b831dfee752b1b17db0a9023b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320208"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="98031-102">Obtention de la classe de message par défaut d’un dossier</span><span class="sxs-lookup"><span data-stu-id="98031-102">Get the default message class of a folder</span></span>

<span data-ttu-id="98031-103">Cet exemple montre comment utiliser la propriété [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) pour obtenir la classe de message par défaut d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="98031-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="98031-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="98031-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="98031-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="98031-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="98031-106">Pour obtenir la classe de message par défaut d’un dossier, utilisez la propriété **DefaultMessageClass** de l’objet [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="98031-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="98031-107">Par exemple, un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) avec IPM.Contact comme **DefaultMessageClass** représente un dossier Contact.</span><span class="sxs-lookup"><span data-stu-id="98031-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="98031-108">Cependant, si le formulaire par défaut du dossier est un formulaire personnalisé ou un formulaire de remplacement, vous devez utiliser l'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) pour déterminer la classe de message du formulaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="98031-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="98031-109">La propriété **DefaultMessageClass** ne renvoie pas la classe de message du formulaire par défaut du dossier.</span><span class="sxs-lookup"><span data-stu-id="98031-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="98031-110">Dans l’exemple de code suivant, la procédure GetDefaultMessageClass utilise **PropertyAccessor** pour déterminer le formulaire par défaut d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="98031-110">In the following code example, the GetDefaultMessageClass procedure uses the **PropertyAccessor** to determine the default form of a folder.</span></span> <span data-ttu-id="98031-111">Si la propriété Folder **PR\_\_\_MsgClass** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) est introuvable et qu'Outlook génère une erreur, le **bloc try... catch** renvoie la propriété **DefaultMessageClass** pour le **dossier**.</span><span class="sxs-lookup"><span data-stu-id="98031-111">If the folder property **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) is not found and Outlook raises an error, the **try…catch** block returns the **DefaultMessageClass** property for the **Folder**.</span></span>

<span data-ttu-id="98031-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="98031-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="98031-113">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="98031-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="98031-114">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="98031-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="98031-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98031-115">See also</span></span>

- [<span data-ttu-id="98031-116">Dossiers</span><span class="sxs-lookup"><span data-stu-id="98031-116">Folders</span></span>](folders.md)

