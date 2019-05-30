---
title: Exemples et scénarios d’automatisation externe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatisation d’InfoPath 2007, de formulaires [InfoPath 2007], ajout de données par programmation, Automation [InfoPath 2007], scénarios externes
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Les membres fournis par l’assembly PIA Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) et l’assembly XML d’interopérabilité d’InfoPath (Microsoft. Office. Interop. InfoPath. Xml. dll) prennent en charge l’écriture de code managé pour l’automatisation InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537814"
---
# <a name="external-automation-scenarios-and-examples"></a>Exemples et scénarios d’automatisation externe

Les membres fournis par l’assembly PIA Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) et l’assembly XML d’interopérabilité d’InfoPath (Microsoft. Office. Interop. InfoPath. Xml. dll) prennent en charge l’écriture de code managé pour l’automatisation InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Établissement de références aux assemblys PIA (Primary Interop Assembly) d’InfoPath de Microsoft Office InfoPath

Pour écrire du code managé pour l’automatisation d’InfoPath, vous devez établir des références à l’interopérabilité principale de Microsoft InfoPath et aux assemblys XML d’interopérabilité d’InfoPath. L’assembly d’interopérabilité de base Microsoft InfoPath fournit une prise en charge de l’interopérabilité avec le modèle objet COM exposé par IPEDITOR. DLL à l’aide des membres de l’espace de noms [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . L’assembly d’interopérabilité XML d’InfoPath offre une prise en charge de l’interopérabilité avec le modèle objet COM exposé par MSXML (Microsoft XML Core Services) à l’aide des membres de l’espace de noms [Microsoft. Office. Interop. InfoPath. xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Les utilisateurs d’applications avec code managé qui automatisent InfoPath doivent disposer d’InfoPath, de l’assembly PIA Microsoft Office InfoPath et de l’assembly XML d’InfoPath Interop installé sur leur ordinateur. L’option **prise en charge** de la programmabilité .net dans le programme d’installation d’InfoPath est définie sur **exécuter à partir du disque dur** pour une installation par défaut d’InfoPath.
>  
> Par conséquent, dans la mesure où le kit de développement logiciel (SDK) .NET Framework 1,1 1,1 ou version ultérieure est installé, ces assemblys d’interopérabilité seront également installés par défaut. Si ces assemblys d’interopérabilité ne sont pas disponibles sur l’ordinateur d’un utilisateur, vous devez vérifier que .NET Framework 1,1 ou une version ultérieure est installé, puis exécuter des **programmes et des fonctionnalités** à partir du **panneau** de configuration pour modifier l’installation et définir la **Programmabilité .net Option de prise en charge** d’InfoPath à **exécuter à partir du disque dur**. 
  
Les procédures suivantes décrivent comment définir des références aux assemblys PIA de Microsoft Office InfoPath et InfoPath XML Interop dans un projet Visual Studio.
  
Pour définir une référence à l’assembly PIA Microsoft. Office. Interop. InfoPath, définissez une référence à la **bibliothèque de types Microsoft InfoPath 3,0** sous l’onglet **com** de la boîte de dialogue **Ajouter une référence** . Même si vous définissez une référence à partir de l’onglet **com** , une référence est établie à l’assembly PIA Microsoft. Office. Interop. InfoPath. dll qui est installé dans le global assembly cache (GAC) par le programme d’installation d’InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Définition d’une référence à l’assembly PIA Microsoft. Office. Interop. InfoPath

1. Ouvrez un projet de code managé Visual Studio.
    
2. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.
    
3. Dans l’onglet **com** , double-cliquez sur **bibliothèque de types Microsoft InfoPath 3,0**, puis cliquez sur **OK**.
    
Pour définir une référence à l’assembly d’interopérabilité Microsoft. Office. Interop. InfoPath. xml, accédez au fichier Microsoft. Office. Interop. InfoPath. Xml. dll qui est installé par défaut dans le _lecteur_<: \Program Files\Microsoft Office\Office14 . Même si vous spécifiez la copie de l’assembly dans le système de fichiers local, cette procédure établit une référence à l’assembly Microsoft. Office. Interop. InfoPath. Xml. dll qui est installé dans le global assembly cache (GAC) par le programme d’installation d’InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Définir une référence à l’assembly d’interopérabilité Microsoft. Office. Interop. InfoPath. Xml

1. Ouvrez ou créez un projet de code managé Visual Studio, tel qu’une **application console** ou une **application Windows**.
    
2. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.
    
3. Sous l’onglet **.net** , cliquez sur **Parcourir**, accédez au dossier < _Drive_>: \Program Files\Microsoft Office\Office14, puis cliquez sur Microsoft. Office. Interop. InfoPath. Xml. dll.
    
4. Cliquez sur **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatiser la modification de la valeur d’un champ

Supposons que l’un des clients de l’utilisateur d’un modèle de formulaire de rapport de ventes InfoPath a récemment changé son nom de «société A» en «société B». Un développeur est invité à écrire du code qui met à jour automatiquement les formulaires de rapport des ventes enregistrés à partir de ce modèle de formulaire pour refléter le changement de nom. Le scénario suivant suppose un formulaire qui contient une zone de texte liée à un champ nommé customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et de formulaire

1. Ouvrez InfoPath et créez un modèle de formulaire vierge.
    
2. Ajoutez un contrôle de **zone de texte** au formulaire, puis nommez le champ lié au contrôle CustomerName.
    
3. Dans le volet Office **champs** , cliquez avec le bouton droit sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.
    
4. Sous l’onglet **Détails** , sélectionnez et copiez la valeur suivante **:**, puis collez-la dans le bloc-notes ou dans un autre emplacement où vous pouvez la récupérer. Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la propriété **SelectionNamespaces** dans votre code. 
    
5. Publiez le modèle de formulaire dans un dossier nommé C:\Test et acceptez le nom par défaut, Template1. 
    
6. Ouvrez le modèle de formulaire, ajoutez le nom «Company A» à la zone de texte liée au champ customerName, puis enregistrez le formulaire sous le nom «Form1». 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Créer une application console de code managé pour remplacer le nom «Company A» par «Company B»

1. Ouvrez Visual Studio et créez une application de console Visual C# ou Visual Basic nommée UpdateCustomer.
    
2. Établissez des références aux assemblys PIA de Microsoft Office InfoPath et InfoPath XML Interop, comme décrit ci-dessus.
    
3. Ajoutez le code suivant au fichier Program.cs ou Module1. vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire. 
    
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
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
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

4. Cliquez sur **Démarrer** le débogage dans le menu Déboguer pour compiler et exécuter l’application console. **** 
    
   L’application ouvre le formulaire enregistré sous la forme Form1. xml et effectue une boucle dans tous les éléments customerName qui contiennent la valeur Company A et modifie cette valeur en Company B. Une fois l’opération terminée, une nouvelle copie du formulaire est enregistrée en tant que Form2. xml dans le dossier C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatiser l’ouverture d’un formulaire et le remplissage des valeurs de champ

L’exemple suivant automatise l’ouverture d’un formulaire vierge et le remplissage des champs prénom, nom et adresse dans le formulaire. Ce scénario suppose un formulaire qui contient trois zones de texte liées à des champs nommés FirstName, LastName et Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et de formulaire

1. Ouvrez InfoPath et créez un formulaire vierge.
    
2. Ajoutez trois contrôles de zone de texte au formulaire, puis nommez les champs liés aux contrôles: FirstName, LastName et Address. Ajoutez les autres champs souhaités.
    
3. Dans le volet Office **champs** , cliquez avec le bouton droit sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.
    
4. Sous l’onglet **Détails** , sélectionnez et copiez la valeur suivante **:**, puis collez-la dans le bloc-notes ou dans un autre emplacement où vous pouvez la récupérer. Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la propriété **SelectionNamespaces** dans votre code. 
    
5. Publiez le modèle de formulaire dans un dossier nommé C:\Temp et acceptez le nom par défaut, Template1.
    
6. Ouvrez le modèle de formulaire et enregistrez un formulaire vierge en tant que «Form1» dans C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Créer une application console de code managé pour ouvrir le formulaire et remplir les champs

1. Ouvrez Visual Studio et créez une application de console Visual C# ou Visual Basic nommée OpenForm.
    
2. Établissez des références aux assemblys PIA de Microsoft Office InfoPath et InfoPath XML Interop, comme décrit ci-dessus.
    
3. Ajoutez le code suivant au fichier Program.cs ou Module1. vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire. 
    
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
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. Dans le **** menu Débogage, cliquez sur Démarrer le débogage pour compiler et exécuter l’application console. **** 
    
   L’application ouvrira le formulaire enregistré sous le nom Form1. xml et renseignez les champs FirstName, LastName et Address avec les valeurs spécifiées dans le code, puis enregistrez le formulaire, en laissant InfoPath Open. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [À propos de l’assembly d’interopérabilité XML InfoPath](about-the-infopath-xml-interop-assembly.md)

