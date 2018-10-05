---
title: Exemples et des scénarios d’automatisation externe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatisation infopath 2007 ajouter par programme des données de formulaires [InfoPath 2007], [InfoPath 2007], l’automatisation externes scénarios
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Les membres fourni par Microsoft Office InfoPath principal assembly d’interopérabilité (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopérabilité XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) prend en charge écrire du code managé pour l’automatisation InfoPath.
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383162"
---
# <a name="external-automation-scenarios-and-examples"></a>Exemples et des scénarios d’automatisation externe

Les membres fourni par Microsoft Office InfoPath principal assembly d’interopérabilité (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopérabilité XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) prend en charge écrire du code managé pour l’automatisation InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Création de références aux assemblys PIA de Microsoft Office InfoPath et InfoPath XML Interop

Pour écrire du code managé pour automatiser InfoPath, vous devez établir des références au PIA Microsoft InfoPath et les assemblys PIA XML InfoPath. L’assembly PIA de Microsoft InfoPath prend en charge l’interopérabilité avec le modèle d’objet COM exposé par IPEDITOR. DLL à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . L’assembly d’interopérabilité XML InfoPath prend en charge l’interopérabilité avec le modèle d’objet COM exposé par Microsoft XML Core Services (MSXML) à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Les utilisateurs des applications de code managé qui automatisent InfoPath doivent avoir l’assembly d’interopérabilité XML InfoPath installé sur leur ordinateur, l’assembly PIA de Microsoft Office InfoPath et InfoPath. L’option de **Prise en charge de la programmabilité .NET** dans le programme d’installation de InfoPath est définie sur **Exécuter à partir du disque dur** pour une installation standard d’InfoPath.
>  
> Par conséquent, que pendant la durée du .NET Framework 1.1 Redistributable ou Kit de développement logiciel (SDK) .NET Framework 1.1 ou version ultérieure est installé, ces assemblys PIA être installés par défaut. Si ces assemblys PIA ne sont pas disponibles sur l’ordinateur d’un utilisateur, vous devez vérifier que le .NET Framework version 1.1 ou ultérieure est installé et puis exécutez des **programmes et fonctionnalités** dans le **Panneau de configuration** pour modifier le programme d’installation et de définir la **la programmabilité .NET Prise en charge** option d’InfoPath pour **Exécuter à partir du disque dur**. 
  
Les procédures suivantes décrivent comment définir des assemblys PIA références pour le PIA de Microsoft Office InfoPath et InfoPath XML dans un projet Visual Studio.
  
Pour définir une référence à l’assembly PIA Microsoft.Office.Interop.InfoPath, définissez une référence à la **Bibliothèque de types Microsoft InfoPath 3.0** sur l’onglet **COM** de la boîte de dialogue **Ajouter une référence** . Même si vous définissez une référence à partir de l’onglet **COM** , une référence est établie à l’assembly PIA Microsoft.Office.Interop.InfoPath.dll qui est installé dans le Global Assembly Cache (GAC) par le programme d’installation InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Définir une référence à l’assembly PIA Microsoft.Office.Interop.InfoPath

1. Ouvrez un projet de code managé de Visual Studio.
    
2. Dans **L’Explorateur de solutions**, cliquez sur **références**, puis cliquez sur **Ajouter une référence**.
    
3. Sous l’onglet **COM** , double-cliquez sur la **Bibliothèque de Type Microsoft InfoPath 3.0**, puis cliquez sur **OK**.
    
Pour définir une référence à l’assembly d’interopérabilité Microsoft.Office.Interop.InfoPath.Xml, recherchez le fichier Microsoft.Office.Interop.InfoPath.Xml.dll qui est installé par défaut dans le < _lecteur_> : \Program Files\Microsoft Office\OFFICE14 dossier . Même si vous spécifiez la copie de l’assembly dans le système de fichiers local, cette procédure établit une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml.dll qui est installé dans le Global Assembly Cache (GAC) par le programme d’installation InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Définir une référence à l’assembly d’interopérabilité Microsoft.Office.Interop.InfoPath.Xml

1. Ouvrez ou créez un projet de code managé Visual Studio, par exemple une **Application de Console** ou une **Application Windows**.
    
2. Dans **L’Explorateur de solutions**, cliquez sur **références**, puis cliquez sur **Ajouter une référence**.
    
3. Sous l’onglet **.NET** , cliquez sur **Parcourir**, accédez au < _lecteur_> : \Program Files\Microsoft Office\OFFICE14 dossier, puis cliquez sur Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Cliquez sur **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatiser la modification de la valeur d’un champ

Supposons qu’un des clients de l’utilisateur d’un modèle de formulaire InfoPath rapport des ventes récemment changé son nom à partir de « Société A » à « société b ». Un développeur est invité à écrire du code qui met automatiquement à jour les formulaires de rapport des ventes enregistrés à partir de ce modèle de formulaire afin de refléter le changement de nom. Le scénario suivant suppose un formulaire contenant une zone de texte qui est liée à un champ nommé nom client.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et le formulaire

1. Ouvrez InfoPath et créer un modèle de formulaire vierge.
    
2. Ajouter un contrôle de **Zone de texte** au formulaire et nommez le champ lié au contrôle engage.
    
3. Dans le volet Office **champs** , cliquez sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.
    
4. Sous l’onglet **Détails** , sélectionnez et copiez la valeur **Namespace :** et le coller dans le bloc-notes ou un autre emplacement où vous pouvez le récupérer. Ultérieurement, vous devrez cette valeur pour définir la valeur de la propriété **SelectionNamespaces** dans votre code. 
    
5. Publier le modèle de formulaire dans un dossier nommé C:\Test et acceptez le nom par défaut, Modèle1. 
    
6. Ouvrez le modèle de formulaire, ajoutez le nom « Société A » à la zone de texte liée au champ Nom client, puis enregistrez le formulaire en tant que « Formulaire1 ». 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Créer une application console de code managé pour modifier le nom à partir de « Société A » à « Société B »

1. Ouvrez Visual Studio et créez un nouveau Visual c# ou Visual Basic Application Console nommée UpdateCustomer.
    
2. Établir des références aux assemblys PIA XML InfoPath et PIA de Microsoft Office InfoPath comme indiqué ci-dessus.
    
3. Ajoutez le code suivant dans le fichier Program.cs ou Module1.vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copié lors de la création de l’exemple de formulaire. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. Dans le menu **Déboguer** pour compiler et exécuter l’application de console, cliquez sur **Démarrer le débogage** . 
    
   L’application s’ouvre le formulaire enregistré en tant que Form1.xml et effectue une boucle sur tous les éléments nom client qui contiennent la valeur de la société A et modifie cette valeur à la société B. Une fois l’opération terminée, une nouvelle copie du formulaire est enregistrée en tant que Form2.xml dans le dossier C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatiser l’ouverture d’un formulaire et le remplissage des valeurs de champ

L’exemple suivant automatise l’ouverture d’un formulaire vierge et remplissage prénom, nom de famille, les champs d’adresse dans l’écran. Ce scénario suppose un formulaire qui contient trois zones de texte qui sont liés à des champs nommés FirstName, LastName et l’adresse.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et le formulaire

1. Ouvrez InfoPath et créez un formulaire vierge.
    
2. Ajouter trois contrôles de zone de texte au formulaire et les champs liés aux contrôles de nom : prénom, nom et adresse. Ajoutez tous les champs que vous souhaitez.
    
3. Dans le volet Office **champs** , cliquez sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.
    
4. Sous l’onglet **Détails** , sélectionnez et copiez la valeur **Namespace :** et le coller dans le bloc-notes ou un autre emplacement où vous pouvez le récupérer. Ultérieurement, vous devrez cette valeur pour définir la valeur de la propriété **SelectionNamespaces** dans votre code. 
    
5. Publier le modèle de formulaire dans un dossier nommé C:\Temp et acceptez le nom par défaut, Modèle1.
    
6. Ouvrez le modèle de formulaire et enregistrer un formulaire vierge en tant que « Formulaire1 » sur C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Créer une application de console de code managé pour ouvrir le formulaire et remplissez les champs

1. Ouvrez Visual Studio et créez un nouveau Visual c# ou Visual Basic Application Console nommée OpenForm.
    
2. Établir des références aux assemblys PIA XML InfoPath et PIA de Microsoft Office InfoPath comme indiqué ci-dessus.
    
3. Ajoutez le code suivant dans le fichier Program.cs ou Module1.vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copié lors de la création de l’exemple de formulaire. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. Dans le menu **Déboguer** , cliquez sur **Démarrer le débogage** pour compiler et exécuter l’application console. 
    
   L’application sera ouvrir le formulaire enregistré en tant que Form1.xml et renseignez les champs FirstName, LastName et adresse avec les valeurs spécifiées dans le code, puis enregistrez le formulaire InfoPath étant ouverte. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [À propos de l’assembly d’interopérabilité XML InfoPath](about-the-infopath-xml-interop-assembly.md)

