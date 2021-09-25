---
title: Exemples et scénarios d’automatisation externe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automating infopath 2007,forms [InfoPath 2007], adding data programmatically,automation [InfoPath 2007], external scenarios
ms.localizationpriority: medium
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Les membres fournis par l’assembly Microsoft Office InfoPath d’interop assembly (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopation XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permettent d’écrire du code géré pour l’automatisation d’InfoPath.
ms.openlocfilehash: da68c9e5924fdc83aee2b700115db03c91cf55fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552121"
---
# <a name="external-automation-scenarios-and-examples"></a>Exemples et scénarios d’automatisation externe

Les membres fournis par l’assembly Microsoft Office InfoPath d’interop assembly (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopation XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permettent d’écrire du code géré pour l’automatisation d’InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Établissement de références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML Interop

Pour écrire du code géré pour l’automatisation d’InfoPath, vous devez établir des références à l’interop principale Microsoft InfoPath et aux assemblys d’interopation XML InfoPath. L’assembly d’interopérabilité principale Microsoft InfoPath assure la prise en charge de l’interopérabilité avec le modèle objet COM exposé par IPEDITOR.DLL à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) L’assembly d’interopérabilité XML InfoPath fournit la prise en charge de l’interopérabilité avec le modèle objet COM exposé par Microsoft XML Core Services® (MSXML) à l’aide des membres de [l’espace de nomsMicrosoft.Office.Interop.InfoPath.Xml.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) 
  
> [!IMPORTANT]
> Les utilisateurs d’applications avec code géré qui automatisent InfoPath doivent avoir installé InfoPath, l’assembly d’interopation principale infoPath Microsoft Office et l’assembly d’opation XML InfoPath sur leurs ordinateurs. L’option Prise en charge de la **programmabilité .NET** dans le programme d’installation d’InfoPath est définie sur Exécuter à partir de **Mon** ordinateur pour une installation classique d’InfoPath.
>  
> Par conséquent, tant que le Kit de développement logiciel (SDK) .NET Framework 1.1 Redistributable ou .NET Framework 1.1 ou ultérieur est installé, ces assemblys d’interopation seront également installés par défaut. Si ces assemblys d’interopation ne sont pas disponibles sur l’ordinateur d’un utilisateur, vous devez vérifier  que le  .NET Framework 1.1 ou ultérieur est installé, puis exécuter Programmes et fonctionnalités à partir du Panneau de configuration pour modifier l’installation et définir l’option prise en charge de la **programmabilité .NET** d’InfoPath pour qu’elle s’exécute à partir du My **Computer**. 
  
Les procédures suivantes décrivent comment définir des références à l’interop principale infoPath Microsoft Office et aux assemblys d’interopation XML InfoPath dans un projet Visual Studio projet.
  
Pour définir une référence à Microsoft. Office’assembly d’opée principale.Interop.InfoPath, définissez une référence à la bibliothèque de types  **Microsoft InfoPath 3.0** sous l’onglet **COM** de la boîte de dialogue Ajouter une référence. Même si vous définissez une référence à partir de l’onglet **COM,** une référence est établie à l’assembly d’interconnexion principale Microsoft.Office.Interop.InfoPath.dll installé dans le Global Assembly Cache (GAC) par le programme d’installation d’InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Définissez une référence à Microsoft. Office assembly d’opation principale.Interop.InfoPath

1. Ouvrez un Visual Studio de code géré.
    
2. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.
    
3. Sous **l’onglet COM,** double-cliquez sur Bibliothèque de types **Microsoft InfoPath 3.0,** puis cliquez sur **OK**.
    
Pour définir une référence à l’assembly d’interopation Microsoft.Office.Interop.InfoPath.Xml, accédez au fichier Microsoft.Office.Interop.InfoPath.Xml.dll installé  par défaut dans le dossier>:\Program Files\Microsoft Office\OFFICE14 du lecteur <. Même si vous spécifiez la copie de l’assembly dans le système de fichiers local, cette procédure établit une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml.dll installé dans le Global Assembly Cache (GAC) par le programme d’installation d’InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Définir une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml op.

1. Ouvrez ou créez un projet Visual Studio code géré, tel qu’une **application console** ou une **application Windows.**
    
2. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.
    
3. Sous l’onglet **.NET,** cliquez sur Parcourir, accédez au lecteur _<_>:\Program Files\Microsoft Office\OFFICE14, puis cliquez sur Microsoft.Office.Interop.InfoPath.Xml.dll. 
    
4. Cliquez sur **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatiser la modification de la valeur d’un champ

Supposons que l’un des clients de l’utilisateur d’un modèle de formulaire de rapport des ventes InfoPath a récemment modifié son nom de « Société A » en « Société B ». Un développeur est invité à écrire du code qui met automatiquement à jour les formulaires de rapport des ventes enregistrés à partir de ce modèle de formulaire pour refléter le changement de nom. Le scénario suivant suppose un formulaire qui contient une zone de texte liée à un champ nommé customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et de formulaire

1. Ouvrez InfoPath et créez un modèle de formulaire vide.
    
2. Ajoutez **un contrôle Zone** de texte au formulaire et nommez le champ lié au contrôle customerName.
    
3. Dans le **volet Des champs,** cliquez avec le bouton droit sur le dossier **myFields,** puis cliquez sur **Propriétés.**
    
4. Sous **l’onglet Détails,** sélectionnez et copiez la valeur suivante Espace de noms : **,** puis collez-la dans Bloc-notes ou dans un autre emplacement où vous pouvez la récupérer. Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la **propriété SelectionNamespaces** dans votre code. 
    
5. Publiez le modèle de formulaire dans un dossier nommé C:\Test et acceptez le nom par défaut, Template1. 
    
6. Ouvrez le modèle de formulaire, ajoutez le nom « Société A » à la zone de texte liée au champ customerName, puis enregistrez le formulaire sous le nom « Form1 ». 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Créer une application console avec code géré pour changer le nom de « Société A » en « Société B »

1. Ouvrez Visual Studio et créez une application console visual C# ou Visual Basic nommée UpdateCustomer.
    
2. Établissez des références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML, comme décrit ci-dessus.
    
3. Ajoutez le code suivant au fichier Program.cs ou Module1.vb, en mettant à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire. 
    
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

4. Cliquez **sur Démarrer le débogage** dans le menu **Débogage** pour compiler et exécuter l’application console. 
    
   L’application ouvre le formulaire enregistré sous Form1.xml et pare en boucle tous les éléments customerName qui contiennent la valeur Company A et modifie cette valeur en Société B. Une fois l’opération terminée, une nouvelle copie du formulaire est enregistrée sous la forme dForm2.xml dans le dossier C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatiser l’ouverture d’un formulaire et le remplissage des valeurs de champ

L’exemple suivant automatise l’ouverture d’un formulaire vierge et le remplit des champs prénom, nom et adresse du formulaire. Ce scénario suppose un formulaire qui contient trois zones de texte liées aux champs FirstName, LastName et Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Créer l’exemple de modèle de formulaire et de formulaire

1. Ouvrez InfoPath et créez un formulaire vide.
    
2. Ajoutez trois contrôles de zone de texte au formulaire et nommez les champs liés aux contrôles : FirstName, LastName et Address. Ajoutez les autres champs de votre recherche.
    
3. Dans le **volet Des champs,** cliquez avec le bouton droit sur le dossier **myFields,** puis cliquez sur **Propriétés.**
    
4. Sous **l’onglet Détails,** sélectionnez et copiez la valeur suivante Espace de noms : **,** puis collez-la dans Bloc-notes ou dans un autre emplacement où vous pouvez la récupérer. Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la **propriété SelectionNamespaces** dans votre code. 
    
5. Publiez le modèle de formulaire dans un dossier nommé C:\Temp et acceptez le nom par défaut, Template1.
    
6. Ouvrez le modèle de formulaire et enregistrez un formulaire vide sous le nom « Form1 » dans C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Créer une application console avec code géré pour ouvrir le formulaire et remplir les champs

1. Ouvrez Visual Studio et créez une application console visual C# ou Visual Basic appelée OpenForm.
    
2. Établissez des références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML, comme décrit ci-dessus.
    
3. Ajoutez le code suivant au fichier Program.cs ou Module1.vb, en mettant à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire. 
    
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

4. Dans le menu **Débogage,** cliquez **sur Démarrer le débogage** pour compiler et exécuter l’application console. 
    
   L’application ouvre le formulaire enregistré en tant que Form1.xml et remplit les champs FirstName, LastName et Address avec les valeurs spécifiées dans le code, puis enregistre le formulaire, en laissant InfoPath ouvert. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [À propos de l’assembly d’interopérabilité XML InfoPath](about-the-infopath-xml-interop-assembly.md)

