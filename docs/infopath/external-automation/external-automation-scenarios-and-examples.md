---
title: Exemples et scénarios d’automatisation externe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automating infopath 2007,forms [InfoPath 2007], adding data programmatically,automation [InfoPath 2007], external scenarios
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Les membres fournis par l’assembly Microsoft Office InfoPath d’interop assembly (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopation XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permettent d’écrire du code géré pour l’automatisation d’InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537814"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="44885-104">Exemples et scénarios d’automatisation externe</span><span class="sxs-lookup"><span data-stu-id="44885-104">External automation scenarios and examples</span></span>

<span data-ttu-id="44885-105">Les membres fournis par l’assembly Microsoft Office InfoPath d’interop assembly (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopation XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permettent d’écrire du code géré pour l’automatisation d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44885-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="44885-106">Établissement de références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML Interop</span><span class="sxs-lookup"><span data-stu-id="44885-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="44885-107">Pour écrire du code géré pour l’automatisation d’InfoPath, vous devez établir des références à l’interop principale Microsoft InfoPath et aux assemblys d’interopation XML InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44885-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="44885-108">L’assembly d’interopérabilité principale Microsoft InfoPath assure la prise en charge de l’interopérabilité avec le modèle objet COM exposé par IPEDITOR.DLL à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)</span><span class="sxs-lookup"><span data-stu-id="44885-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="44885-109">L’assembly d’interopérabilité XML InfoPath fournit la prise en charge de l’interopérabilité avec le modèle objet COM exposé par Microsoft XML Core Services® (MSXML) à l’aide des membres de [l’espace de nomsMicrosoft.Office.Interop.InfoPath.Xml.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)</span><span class="sxs-lookup"><span data-stu-id="44885-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="44885-110">Les utilisateurs d’applications avec code géré qui automatisent InfoPath doivent avoir Installé InfoPath, l’assembly d’interopation principale infoPath Microsoft Office et l’assembly d’interopation XML InfoPath sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="44885-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="44885-111">L’option Prise en charge de **la programmabilité .NET** dans le programme d’installation d’InfoPath est définie sur Exécuter à partir du My **Computer** pour une installation classique d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44885-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="44885-112">Par conséquent, tant que le Kit de développement logiciel (SDK) .NET Framework 1.1 Redistributable ou .NET Framework 1.1 ou ultérieur est installé, ces assemblys d’interopation seront également installés par défaut.</span><span class="sxs-lookup"><span data-stu-id="44885-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="44885-113">Si ces assemblys d’interopation ne sont pas disponibles sur l’ordinateur d’un utilisateur, vous devez vérifier  que le  .NET Framework 1.1 ou ultérieur est installé, puis exécuter Programmes et fonctionnalités à partir du Panneau de configuration pour modifier l’installation et définir l’option prise en charge de la **programmabilité .NET** d’InfoPath pour qu’elle s’exécute à partir du My **Computer**.</span><span class="sxs-lookup"><span data-stu-id="44885-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="44885-114">Les procédures suivantes décrivent comment définir des références à l’interop principale infoPath Microsoft Office et aux assemblys d’interopation XML InfoPath dans un projet Visual Studio projet.</span><span class="sxs-lookup"><span data-stu-id="44885-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="44885-115">Pour définir une référence à Microsoft. Office’assembly d’opée principale.Interop.InfoPath, définissez une référence à la bibliothèque de types  **Microsoft InfoPath 3.0** sous l’onglet **COM** de la boîte de dialogue Ajouter une référence.</span><span class="sxs-lookup"><span data-stu-id="44885-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="44885-116">Même si vous définissez une référence à partir de l’onglet **COM,** une référence est établie à l’assembly d’interconnexion principale Microsoft.Office.Interop.InfoPath.dll installé dans le Global Assembly Cache (GAC) par le programme d’installation d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44885-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="44885-117">Définissez une référence à Microsoft. Office assembly d’opation principale.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="44885-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="44885-118">Ouvrez un Visual Studio de code géré.</span><span class="sxs-lookup"><span data-stu-id="44885-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="44885-119">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="44885-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="44885-120">Sous **l’onglet COM,** double-cliquez sur Bibliothèque de types **Microsoft InfoPath 3.0,** puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="44885-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="44885-121">Pour définir une référence à l’assembly d’interopation Microsoft.Office.Interop.InfoPath.Xml, accédez au fichier Microsoft.Office.Interop.InfoPath.Xml.dll installé  par défaut dans le dossier>:\Program Files\Microsoft Office\OFFICE14 du lecteur <.</span><span class="sxs-lookup"><span data-stu-id="44885-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="44885-122">Même si vous spécifiez la copie de l’assembly dans le système de fichiers local, cette procédure établit une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml.dll installé dans le Global Assembly Cache (GAC) par le programme d’installation d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44885-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="44885-123">Définir une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml op.</span><span class="sxs-lookup"><span data-stu-id="44885-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="44885-124">Ouvrez ou créez un Visual Studio de code géré, tel qu’une **application console** ou une **application Windows.**</span><span class="sxs-lookup"><span data-stu-id="44885-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="44885-125">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur **Références**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="44885-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="44885-126">Sous l’onglet **.NET,** cliquez sur Parcourir, accédez au lecteur _<_>:\Program Files\Microsoft Office\OFFICE14, puis cliquez sur Microsoft.Office.Interop.InfoPath.Xml.dll. </span><span class="sxs-lookup"><span data-stu-id="44885-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="44885-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="44885-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="44885-128">Automatiser la modification de la valeur d’un champ</span><span class="sxs-lookup"><span data-stu-id="44885-128">Automate changing the value of a field</span></span>

<span data-ttu-id="44885-129">Supposons que l’un des clients de l’utilisateur d’un modèle de formulaire de rapport des ventes InfoPath a récemment modifié son nom de « Société A » en « Société B ».</span><span class="sxs-lookup"><span data-stu-id="44885-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="44885-130">Un développeur est invité à écrire du code qui met automatiquement à jour les formulaires de rapport des ventes enregistrés à partir de ce modèle de formulaire pour refléter le changement de nom.</span><span class="sxs-lookup"><span data-stu-id="44885-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="44885-131">Le scénario suivant suppose un formulaire qui contient une zone de texte liée à un champ nommé customerName.</span><span class="sxs-lookup"><span data-stu-id="44885-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="44885-132">Créer l’exemple de modèle de formulaire et de formulaire</span><span class="sxs-lookup"><span data-stu-id="44885-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="44885-133">Ouvrez InfoPath et créez un modèle de formulaire vide.</span><span class="sxs-lookup"><span data-stu-id="44885-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="44885-134">Ajoutez **un contrôle Zone** de texte au formulaire et nommez le champ lié au contrôle customerName.</span><span class="sxs-lookup"><span data-stu-id="44885-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="44885-135">Dans le **volet Des champs,** cliquez avec le bouton droit sur le dossier **myFields,** puis cliquez sur **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="44885-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="44885-136">Sous **l’onglet Détails,** sélectionnez et copiez la valeur suivante Espace de noms : **,** puis collez-la dans Bloc-notes ou dans un autre emplacement où vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="44885-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="44885-137">Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la **propriété SelectionNamespaces** dans votre code.</span><span class="sxs-lookup"><span data-stu-id="44885-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="44885-138">Publiez le modèle de formulaire dans un dossier nommé C:\Test et acceptez le nom par défaut, Template1.</span><span class="sxs-lookup"><span data-stu-id="44885-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="44885-139">Ouvrez le modèle de formulaire, ajoutez le nom « Société A » à la zone de texte liée au champ customerName, puis enregistrez le formulaire sous le nom « Form1 ».</span><span class="sxs-lookup"><span data-stu-id="44885-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="44885-140">Créer une application console avec code géré pour changer le nom de « Société A » en « Société B »</span><span class="sxs-lookup"><span data-stu-id="44885-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="44885-141">Ouvrez Visual Studio et créez une application console visual C# ou Visual Basic nommée UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="44885-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="44885-142">Établissez des références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="44885-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="44885-143">Ajoutez le code suivant au fichier Program.cs ou Module1.vb, en mettant à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire.</span><span class="sxs-lookup"><span data-stu-id="44885-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="44885-144">Cliquez **sur Démarrer le débogage** dans le menu **Débogage** pour compiler et exécuter l’application console.</span><span class="sxs-lookup"><span data-stu-id="44885-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="44885-145">L’application ouvre le formulaire enregistré sous Form1.xml et pare en boucle tous les éléments customerName qui contiennent la valeur Company A et modifie cette valeur en Société B. Une fois l’opération terminée, une nouvelle copie du formulaire est enregistrée Form2.xml dans le dossier C:\Test.</span><span class="sxs-lookup"><span data-stu-id="44885-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="44885-146">Automatiser l’ouverture d’un formulaire et le remplissage des valeurs de champ</span><span class="sxs-lookup"><span data-stu-id="44885-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="44885-147">L’exemple suivant automatise l’ouverture d’un formulaire vierge et le remplit des champs prénom, nom et adresse du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44885-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="44885-148">Ce scénario suppose un formulaire qui contient trois zones de texte liées aux champs FirstName, LastName et Address.</span><span class="sxs-lookup"><span data-stu-id="44885-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="44885-149">Créer l’exemple de modèle de formulaire et de formulaire</span><span class="sxs-lookup"><span data-stu-id="44885-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="44885-150">Ouvrez InfoPath et créez un formulaire vide.</span><span class="sxs-lookup"><span data-stu-id="44885-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="44885-151">Ajoutez trois contrôles de zone de texte au formulaire et nommez les champs liés aux contrôles : FirstName, LastName et Address.</span><span class="sxs-lookup"><span data-stu-id="44885-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="44885-152">Ajoutez les autres champs de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="44885-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="44885-153">Dans le **volet Des champs,** cliquez avec le bouton droit sur le dossier **myFields,** puis cliquez sur **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="44885-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="44885-154">Sous **l’onglet Détails,** sélectionnez et copiez la valeur suivante Espace de noms : **,** puis collez-la dans Bloc-notes ou dans un autre emplacement où vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="44885-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="44885-155">Vous aurez besoin de cette valeur ultérieurement pour définir la valeur de la **propriété SelectionNamespaces** dans votre code.</span><span class="sxs-lookup"><span data-stu-id="44885-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="44885-156">Publiez le modèle de formulaire dans un dossier nommé C:\Temp et acceptez le nom par défaut, Template1.</span><span class="sxs-lookup"><span data-stu-id="44885-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="44885-157">Ouvrez le modèle de formulaire et enregistrez un formulaire vide sous le nom « Form1 » dans C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="44885-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="44885-158">Créer une application console avec code géré pour ouvrir le formulaire et remplir les champs</span><span class="sxs-lookup"><span data-stu-id="44885-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="44885-159">Ouvrez Visual Studio et créez une application console visual C# ou Visual Basic appelée OpenForm.</span><span class="sxs-lookup"><span data-stu-id="44885-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="44885-160">Établissez des références aux assemblys Microsoft Office’interop principale InfoPath et InfoPath XML, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="44885-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="44885-161">Ajoutez le code suivant au fichier Program.cs ou Module1.vb, en mettant à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copiée lors de la création de l’exemple de formulaire.</span><span class="sxs-lookup"><span data-stu-id="44885-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="44885-162">Dans le menu **Débogage,** cliquez **sur Démarrer le débogage** pour compiler et exécuter l’application console.</span><span class="sxs-lookup"><span data-stu-id="44885-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="44885-163">L’application ouvre le formulaire enregistré en tant que Form1.xml et remplit les champs FirstName, LastName et Address avec les valeurs spécifiées dans le code, puis enregistre le formulaire, en laissant InfoPath ouvert.</span><span class="sxs-lookup"><span data-stu-id="44885-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="44885-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44885-164">See also</span></span>

- [<span data-ttu-id="44885-165">À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="44885-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="44885-166">À propos de l’assembly d’interopérabilité XML InfoPath</span><span class="sxs-lookup"><span data-stu-id="44885-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

