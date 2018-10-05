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
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="98935-104">Exemples et des scénarios d’automatisation externe</span><span class="sxs-lookup"><span data-stu-id="98935-104">External automation scenarios and examples</span></span>

<span data-ttu-id="98935-105">Les membres fourni par Microsoft Office InfoPath principal assembly d’interopérabilité (Microsoft.Office.Interop.InfoPath.dll) et l’assembly d’interopérabilité XML InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) prend en charge écrire du code managé pour l’automatisation InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="98935-106">Création de références aux assemblys PIA de Microsoft Office InfoPath et InfoPath XML Interop</span><span class="sxs-lookup"><span data-stu-id="98935-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="98935-107">Pour écrire du code managé pour automatiser InfoPath, vous devez établir des références au PIA Microsoft InfoPath et les assemblys PIA XML InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="98935-108">L’assembly PIA de Microsoft InfoPath prend en charge l’interopérabilité avec le modèle d’objet COM exposé par IPEDITOR. DLL à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="98935-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="98935-109">L’assembly d’interopérabilité XML InfoPath prend en charge l’interopérabilité avec le modèle d’objet COM exposé par Microsoft XML Core Services (MSXML) à l’aide des membres de l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="98935-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="98935-110">Les utilisateurs des applications de code managé qui automatisent InfoPath doivent avoir l’assembly d’interopérabilité XML InfoPath installé sur leur ordinateur, l’assembly PIA de Microsoft Office InfoPath et InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="98935-111">L’option de **Prise en charge de la programmabilité .NET** dans le programme d’installation de InfoPath est définie sur **Exécuter à partir du disque dur** pour une installation standard d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="98935-112">Par conséquent, que pendant la durée du .NET Framework 1.1 Redistributable ou Kit de développement logiciel (SDK) .NET Framework 1.1 ou version ultérieure est installé, ces assemblys PIA être installés par défaut.</span><span class="sxs-lookup"><span data-stu-id="98935-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="98935-113">Si ces assemblys PIA ne sont pas disponibles sur l’ordinateur d’un utilisateur, vous devez vérifier que le .NET Framework version 1.1 ou ultérieure est installé et puis exécutez des **programmes et fonctionnalités** dans le **Panneau de configuration** pour modifier le programme d’installation et de définir la **la programmabilité .NET Prise en charge** option d’InfoPath pour **Exécuter à partir du disque dur**.</span><span class="sxs-lookup"><span data-stu-id="98935-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="98935-114">Les procédures suivantes décrivent comment définir des assemblys PIA références pour le PIA de Microsoft Office InfoPath et InfoPath XML dans un projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="98935-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="98935-115">Pour définir une référence à l’assembly PIA Microsoft.Office.Interop.InfoPath, définissez une référence à la **Bibliothèque de types Microsoft InfoPath 3.0** sur l’onglet **COM** de la boîte de dialogue **Ajouter une référence** .</span><span class="sxs-lookup"><span data-stu-id="98935-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="98935-116">Même si vous définissez une référence à partir de l’onglet **COM** , une référence est établie à l’assembly PIA Microsoft.Office.Interop.InfoPath.dll qui est installé dans le Global Assembly Cache (GAC) par le programme d’installation InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="98935-117">Définir une référence à l’assembly PIA Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="98935-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="98935-118">Ouvrez un projet de code managé de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="98935-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="98935-119">Dans **L’Explorateur de solutions**, cliquez sur **références**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="98935-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="98935-120">Sous l’onglet **COM** , double-cliquez sur la **Bibliothèque de Type Microsoft InfoPath 3.0**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="98935-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="98935-121">Pour définir une référence à l’assembly d’interopérabilité Microsoft.Office.Interop.InfoPath.Xml, recherchez le fichier Microsoft.Office.Interop.InfoPath.Xml.dll qui est installé par défaut dans le < _lecteur_> : \Program Files\Microsoft Office\OFFICE14 dossier .</span><span class="sxs-lookup"><span data-stu-id="98935-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="98935-122">Même si vous spécifiez la copie de l’assembly dans le système de fichiers local, cette procédure établit une référence à l’assembly Microsoft.Office.Interop.InfoPath.Xml.dll qui est installé dans le Global Assembly Cache (GAC) par le programme d’installation InfoPath.</span><span class="sxs-lookup"><span data-stu-id="98935-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="98935-123">Définir une référence à l’assembly d’interopérabilité Microsoft.Office.Interop.InfoPath.Xml</span><span class="sxs-lookup"><span data-stu-id="98935-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="98935-124">Ouvrez ou créez un projet de code managé Visual Studio, par exemple une **Application de Console** ou une **Application Windows**.</span><span class="sxs-lookup"><span data-stu-id="98935-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="98935-125">Dans **L’Explorateur de solutions**, cliquez sur **références**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="98935-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="98935-126">Sous l’onglet **.NET** , cliquez sur **Parcourir**, accédez au < _lecteur_> : \Program Files\Microsoft Office\OFFICE14 dossier, puis cliquez sur Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="98935-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="98935-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="98935-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="98935-128">Automatiser la modification de la valeur d’un champ</span><span class="sxs-lookup"><span data-stu-id="98935-128">Automate changing the value of a field</span></span>

<span data-ttu-id="98935-129">Supposons qu’un des clients de l’utilisateur d’un modèle de formulaire InfoPath rapport des ventes récemment changé son nom à partir de « Société A » à « société b ».</span><span class="sxs-lookup"><span data-stu-id="98935-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="98935-130">Un développeur est invité à écrire du code qui met automatiquement à jour les formulaires de rapport des ventes enregistrés à partir de ce modèle de formulaire afin de refléter le changement de nom.</span><span class="sxs-lookup"><span data-stu-id="98935-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="98935-131">Le scénario suivant suppose un formulaire contenant une zone de texte qui est liée à un champ nommé nom client.</span><span class="sxs-lookup"><span data-stu-id="98935-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="98935-132">Créer l’exemple de modèle de formulaire et le formulaire</span><span class="sxs-lookup"><span data-stu-id="98935-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="98935-133">Ouvrez InfoPath et créer un modèle de formulaire vierge.</span><span class="sxs-lookup"><span data-stu-id="98935-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="98935-134">Ajouter un contrôle de **Zone de texte** au formulaire et nommez le champ lié au contrôle engage.</span><span class="sxs-lookup"><span data-stu-id="98935-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="98935-135">Dans le volet Office **champs** , cliquez sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="98935-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="98935-136">Sous l’onglet **Détails** , sélectionnez et copiez la valeur **Namespace :** et le coller dans le bloc-notes ou un autre emplacement où vous pouvez le récupérer.</span><span class="sxs-lookup"><span data-stu-id="98935-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="98935-137">Ultérieurement, vous devrez cette valeur pour définir la valeur de la propriété **SelectionNamespaces** dans votre code.</span><span class="sxs-lookup"><span data-stu-id="98935-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="98935-138">Publier le modèle de formulaire dans un dossier nommé C:\Test et acceptez le nom par défaut, Modèle1.</span><span class="sxs-lookup"><span data-stu-id="98935-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="98935-139">Ouvrez le modèle de formulaire, ajoutez le nom « Société A » à la zone de texte liée au champ Nom client, puis enregistrez le formulaire en tant que « Formulaire1 ».</span><span class="sxs-lookup"><span data-stu-id="98935-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="98935-140">Créer une application console de code managé pour modifier le nom à partir de « Société A » à « Société B »</span><span class="sxs-lookup"><span data-stu-id="98935-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="98935-141">Ouvrez Visual Studio et créez un nouveau Visual c# ou Visual Basic Application Console nommée UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="98935-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="98935-142">Établir des références aux assemblys PIA XML InfoPath et PIA de Microsoft Office InfoPath comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="98935-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="98935-143">Ajoutez le code suivant dans le fichier Program.cs ou Module1.vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copié lors de la création de l’exemple de formulaire.</span><span class="sxs-lookup"><span data-stu-id="98935-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="98935-144">Dans le menu **Déboguer** pour compiler et exécuter l’application de console, cliquez sur **Démarrer le débogage** .</span><span class="sxs-lookup"><span data-stu-id="98935-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="98935-145">L’application s’ouvre le formulaire enregistré en tant que Form1.xml et effectue une boucle sur tous les éléments nom client qui contiennent la valeur de la société A et modifie cette valeur à la société B. Une fois l’opération terminée, une nouvelle copie du formulaire est enregistrée en tant que Form2.xml dans le dossier C:\Test.</span><span class="sxs-lookup"><span data-stu-id="98935-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="98935-146">Automatiser l’ouverture d’un formulaire et le remplissage des valeurs de champ</span><span class="sxs-lookup"><span data-stu-id="98935-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="98935-147">L’exemple suivant automatise l’ouverture d’un formulaire vierge et remplissage prénom, nom de famille, les champs d’adresse dans l’écran.</span><span class="sxs-lookup"><span data-stu-id="98935-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="98935-148">Ce scénario suppose un formulaire qui contient trois zones de texte qui sont liés à des champs nommés FirstName, LastName et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="98935-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="98935-149">Créer l’exemple de modèle de formulaire et le formulaire</span><span class="sxs-lookup"><span data-stu-id="98935-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="98935-150">Ouvrez InfoPath et créez un formulaire vierge.</span><span class="sxs-lookup"><span data-stu-id="98935-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="98935-151">Ajouter trois contrôles de zone de texte au formulaire et les champs liés aux contrôles de nom : prénom, nom et adresse.</span><span class="sxs-lookup"><span data-stu-id="98935-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="98935-152">Ajoutez tous les champs que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="98935-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="98935-153">Dans le volet Office **champs** , cliquez sur le dossier **mesChamps** , puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="98935-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="98935-154">Sous l’onglet **Détails** , sélectionnez et copiez la valeur **Namespace :** et le coller dans le bloc-notes ou un autre emplacement où vous pouvez le récupérer.</span><span class="sxs-lookup"><span data-stu-id="98935-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="98935-155">Ultérieurement, vous devrez cette valeur pour définir la valeur de la propriété **SelectionNamespaces** dans votre code.</span><span class="sxs-lookup"><span data-stu-id="98935-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="98935-156">Publier le modèle de formulaire dans un dossier nommé C:\Temp et acceptez le nom par défaut, Modèle1.</span><span class="sxs-lookup"><span data-stu-id="98935-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="98935-157">Ouvrez le modèle de formulaire et enregistrer un formulaire vierge en tant que « Formulaire1 » sur C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="98935-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="98935-158">Créer une application de console de code managé pour ouvrir le formulaire et remplissez les champs</span><span class="sxs-lookup"><span data-stu-id="98935-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="98935-159">Ouvrez Visual Studio et créez un nouveau Visual c# ou Visual Basic Application Console nommée OpenForm.</span><span class="sxs-lookup"><span data-stu-id="98935-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="98935-160">Établir des références aux assemblys PIA XML InfoPath et PIA de Microsoft Office InfoPath comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="98935-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="98935-161">Ajoutez le code suivant dans le fichier Program.cs ou Module1.vb, en veillant à mettre à jour la valeur de l’espace de noms dans le paramètre de la propriété **SelectionNamespaces** avec la valeur que vous avez copié lors de la création de l’exemple de formulaire.</span><span class="sxs-lookup"><span data-stu-id="98935-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="98935-162">Dans le menu **Déboguer** , cliquez sur **Démarrer le débogage** pour compiler et exécuter l’application console.</span><span class="sxs-lookup"><span data-stu-id="98935-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="98935-163">L’application sera ouvrir le formulaire enregistré en tant que Form1.xml et renseignez les champs FirstName, LastName et adresse avec les valeurs spécifiées dans le code, puis enregistrez le formulaire InfoPath étant ouverte.</span><span class="sxs-lookup"><span data-stu-id="98935-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="98935-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98935-164">See also</span></span>

- [<span data-ttu-id="98935-165">À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="98935-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="98935-166">À propos de l’assembly d’interopérabilité XML InfoPath</span><span class="sxs-lookup"><span data-stu-id="98935-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

