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
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Synchroniser Outlook avec un dossier SharePoint

Cet exemple montre comment se connecter par programme Outlook avec un dossier SharePoint et synchroniser les contenus du dossier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans Outlook, vous pouvez synchroniser des calendriers, des listes de contacts, des listes de tâches, des forums de discussion ainsi que des bibliothèques de documents vers des dossiers SharePoint. Sur la base de l'URL fournie lors de la synchronisation, Outlook crée un nouveau dossier ayant le même type de base que le dossier SharePoint. Par exemple, la synchronisation à un dossier de calendrier SharePoint crée un dossier calendrier dans Outlook. Les dossiers de synchronisation SharePoint sont stockés dans leur propre fichier de dossiers personnels Outlook (.pst) en dehors de la boîte aux lettres de l'utilisateur. Vous pouvez vous connecter à un dossier SharePoint à l’aide de la [OpenSharedFolder (Chaîne, Objet, Objet, Objet)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) méthode de l’objet d’[espace de noms](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Notez que vous devez utiliser une URL stssync:// qui fournit des détails sur le serveur SharePoint, le chemin d'accès du dossier et d'autres informations nécessaires à Outlook pour ouvrir un dossier SharePoint.

Lors de la connexion à un dossier SharePoint par programmation, vous devez déterminer l'URL correcte à utiliser pour créer la relation de partage. Étant donné que la stssync : / / URL n’est pas fournie pour le dossier dans l’interface utilisateur SharePoint, associez manuellement le dossier de destination dans Outlook. Utilisez ensuite la première procédure, DisplaySharePointUrl, dans l'exemple de code suivant, pour obtenir l'URL correcte. DisplaySharePointUrl utilise l'[Objet](https://msdn.microsoft.com/library/bb652856\(v=office.15\))tableau pour rechercher les informations de liaison de partage dans le dossier actif pour la fenêtre d'explorateur actuelle. Si un ou plusieurs contextes de liaison sont trouvées, les URLs pour tous les contextes partage disponibles apparaissent.

Vous disposez à présent de l’URL appropriée pour créer la relation de partage. Pour synchroniser le nouveau dossier SharePoint dans Outlook, copiez et collez l'URL pour l'affecter à la variable de type chaîne   dans la deuxième procédure, AddSpsFolder. AddSpsFolder automatise la synchronisation du nouveau dossier SharePoint dans Outlook à l'aide de la méthode **NameSpace.OpenSharedFolder**avec une`stssync://`URL (dans ce cas, l'URL produite par la procédure DisplaySharePointUrl ). AddSpsFolderalso fournit aussi un nom de dossier personnalisé, « Example SPS Calendar » (Exemple de calendrier SPS), et spécifie à Outlook d'utiliser la durée de vie par défaut(TTL) pour le dossier. Les dossiers SharePoint téléchargent toujours les pièces jointes d’élément, afin que vous ne deviez pas à le spécifier ici.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Partage de groupe](group-sharing.md)

