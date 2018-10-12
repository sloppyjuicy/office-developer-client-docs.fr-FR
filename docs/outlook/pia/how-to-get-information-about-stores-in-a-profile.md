---
title: Obtenir des informations sur les magasins dans un profil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406567"
---
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="3837d-102">Obtenir des informations sur les magasins dans un profil</span><span class="sxs-lookup"><span data-stu-id="3837d-102">Get information about stores in a profile</span></span>

<span data-ttu-id="3837d-103">Cet exemple montre comment obtenir et énumérer les magasins dans un profil.</span><span class="sxs-lookup"><span data-stu-id="3837d-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="3837d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="3837d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3837d-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3837d-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="3837d-106">Vous pouvez utiliser la collection [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) pour énumérer les magasins pour un profil donné.</span><span class="sxs-lookup"><span data-stu-id="3837d-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="3837d-107">La collection **Stores** fournit des membres qui exposent des informations sur chaque objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , telles que le moment où un objet **Store** a été ajouté ou le moment où un objet **Store** va être supprimé du profil actif.</span><span class="sxs-lookup"><span data-stu-id="3837d-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="3837d-108">Dans l’exemple de code suivant, EnumerateStores obtient l’objet **Stores** qui représente les magasins du profil actif, et énumère les magasins.</span><span class="sxs-lookup"><span data-stu-id="3837d-108">In the following code example,   gets the Stores object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="3837d-109">L'objet EnumerateStores examine chaque objet **Store** de la collection **Stores**.</span><span class="sxs-lookup"><span data-stu-id="3837d-109"> examines each Store object in the Stores collection.</span></span> <span data-ttu-id="3837d-110">Si la propriété [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) retourne **true**, indiquant qu'il existe une banque avec une extension .pst ou .ost, les propriétés [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) et [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) sont écrites sur les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="3837d-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="3837d-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3837d-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="3837d-112">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="3837d-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="3837d-113">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="3837d-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3837d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3837d-114">See also</span></span>

- [<span data-ttu-id="3837d-115">Magasins</span><span class="sxs-lookup"><span data-stu-id="3837d-115">Stores</span></span>](stores.md)

