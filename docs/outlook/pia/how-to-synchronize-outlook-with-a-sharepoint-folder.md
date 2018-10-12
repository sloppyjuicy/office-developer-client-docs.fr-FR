---
title: Synchroniser Outlook avec un dossier SharePoint
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d7fdf4f6cf9d6d473257d335ce968ce8f518ebe2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407176"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="0b01b-102">Synchroniser Outlook avec un dossier SharePoint</span><span class="sxs-lookup"><span data-stu-id="0b01b-102">How to: Synchronize Outlook with a SharePoint Folder</span></span>

<span data-ttu-id="0b01b-103">Cet exemple montre comment se connecter par programme Outlook avec un dossier SharePoint et synchroniser les contenus du dossier.</span><span class="sxs-lookup"><span data-stu-id="0b01b-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="0b01b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b01b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0b01b-105">L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0b01b-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="0b01b-106">Dans Outlook, vous pouvez synchroniser des calendriers, des listes de contacts, des listes de tâches, des forums de discussion ainsi que des bibliothèques de documents vers des dossiers SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0b01b-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="0b01b-107">Sur la base de l'URL fournie lors de la synchronisation, Outlook crée un nouveau dossier ayant le même type de base que le dossier SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0b01b-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="0b01b-108">Par exemple, la synchronisation à un dossier de calendrier SharePoint crée un dossier calendrier dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="0b01b-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="0b01b-109">Les dossiers de synchronisation SharePoint sont stockés dans leur propre fichier de dossiers personnels Outlook (.pst) en dehors de la boîte aux lettres de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b01b-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user's mailbox.</span></span> <span data-ttu-id="0b01b-110">Vous pouvez vous connecter à un dossier SharePoint à l’aide de la [OpenSharedFolder (Chaîne, Objet, Objet, Objet)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) méthode de l’objet d’[espace de noms](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0b01b-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="0b01b-111">Notez que vous devez utiliser une URL stssync:// qui fournit des détails sur le serveur SharePoint, le chemin d'accès du dossier et d'autres informations nécessaires à Outlook pour ouvrir un dossier SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0b01b-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="0b01b-112">Lors de la connexion à un dossier SharePoint par programmation, vous devez déterminer l'URL correcte à utiliser pour créer la relation de partage.</span><span class="sxs-lookup"><span data-stu-id="0b01b-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="0b01b-113">Étant donné que la stssync : / / URL n’est pas fournie pour le dossier dans l’interface utilisateur SharePoint, associez manuellement le dossier de destination dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="0b01b-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="0b01b-114">Utilisez ensuite la première procédure, DisplaySharePointUrl, dans l'exemple de code suivant, pour obtenir l'URL correcte.</span><span class="sxs-lookup"><span data-stu-id="0b01b-114">Then use the first procedure,  , in the following code example, to get the correct URL.</span></span> <span data-ttu-id="0b01b-115">DisplaySharePointUrl utilise l'[Objet](https://msdn.microsoft.com/library/bb652856\(v=office.15\))tableau pour rechercher les informations de liaison de partage dans le dossier actif pour la fenêtre d'explorateur actuelle.</span><span class="sxs-lookup"><span data-stu-id="0b01b-115"> uses the Table object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="0b01b-116">Si un ou plusieurs contextes de liaison sont trouvées, les URLs pour tous les contextes partage disponibles apparaissent.</span><span class="sxs-lookup"><span data-stu-id="0b01b-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="0b01b-117">Vous disposez à présent de l’URL appropriée pour créer la relation de partage.</span><span class="sxs-lookup"><span data-stu-id="0b01b-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="0b01b-118">Pour synchroniser le nouveau dossier SharePoint dans Outlook, copiez et collez l'URL pour l'affecter à la variable de type chaîne   dans la deuxième procédure, AddSpsFolder.</span><span class="sxs-lookup"><span data-stu-id="0b01b-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable   in the second procedure,  .</span></span> <span data-ttu-id="0b01b-119">AddSpsFolder automatise la synchronisation du nouveau dossier SharePoint dans Outlook à l'aide de la méthode **NameSpace.OpenSharedFolder**avec une`stssync://`URL (dans ce cas, l'URL produite par la procédure DisplaySharePointUrl ).</span><span class="sxs-lookup"><span data-stu-id="0b01b-119"> automates the synchronization of the new SharePoint folder in Outlook by using the NameSpace.OpenSharedFolder method with a stssync:// URL (in this case, the URL produced by the   procedure).</span></span> <span data-ttu-id="0b01b-120">AddSpsFolderalso fournit aussi un nom de dossier personnalisé, « Example SPS Calendar » (Exemple de calendrier SPS), et spécifie à Outlook d'utiliser la durée de vie par défaut(TTL) pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="0b01b-120">also provides a custom folder name, "Example SPS Calendar", and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="0b01b-121">Les dossiers SharePoint téléchargent toujours les pièces jointes d’élément, afin que vous ne deviez pas à le spécifier ici.</span><span class="sxs-lookup"><span data-stu-id="0b01b-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="0b01b-122">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0b01b-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0b01b-123">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="0b01b-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0b01b-124">La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="0b01b-124">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "https://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="0b01b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b01b-125">See also</span></span>

- [<span data-ttu-id="0b01b-126">Partage de groupe</span><span class="sxs-lookup"><span data-stu-id="0b01b-126">Group Sharing</span></span>](group-sharing.md)

