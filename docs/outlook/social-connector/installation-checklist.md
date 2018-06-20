---
title: Liste de vérification d’installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Cette rubrique décrit les conditions requises pour installer correctement un fournisseur Outlook Social Connector (OSC) et l’installation vérifie que votre programme d’installation du fournisseur doit effectuer pour fonctionner correctement.
ms.openlocfilehash: cb8ed24db28c3b0e945c4db4b2daa4a2470d7dd5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787595"
---
# <a name="installation-checklist"></a>Liste de vérification d’installation

Cette rubrique décrit les conditions requises pour installer correctement un fournisseur Outlook Social Connector (OSC) et l’installation vérifie que votre programme d’installation du fournisseur doit effectuer pour fonctionner correctement.
  
## <a name="installation-overview"></a>Présentation de l’installation

Les utilisateurs doivent installer fournisseurs OSC uniquement si une version prise en charge d’Outlook est présente et l’OSC est installé et activé sur l’ordinateur client. Prise en charge des versions d’Outlook sont Office Outlook 2003, Microsoft Office Outlook 2007, Outlook 2010 et Outlook 2013 (installé sur l’ordinateur client ou, dans le cas d’Outlook 2010 et Outlook 2013, livré par Click-to-Run sur l’ordinateur client). Pour garantir la réussite de l’installation, le programme d’installation de votre fournisseur doit effectuer les opérations suivantes :
  
- Vérifiez si une version prise en charge d’Outlook.
    
- Vérifiez si l’OSC est installé.
    
> [!NOTE]
> Click-to-Run est un environnement virtuel dans lequel Outlook 2010 (32 bits) ou Outlook 2013 (32 bits) peut s’exécuter. Pour Outlook 2013, vérifiez si la clé VirtualOutlook existe dans HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook du Registre Windows. Pour plus d’informations sur la fourniture d’Outlook en tant que Click-to-Run produit sur un ordinateur client, voir [comment vérifier si Outlook est disponible sur un ordinateur en tant que Click-to-Run produit](http://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Toutefois, l’utilisateur, doit vous assurer que l’OSC est activé avant d’installer le fournisseur.
  
Les tierces parties, y compris les fournisseurs OSC, ne peuvent pas redistribuer le OSC. Toutefois, si l’OSC n’est pas installé, le programme d’installation du fournisseur pouvez utiliser g-liens appropriés pour installer l’OSC sur l’ordinateur client. Un lien g est une URL spéciale sur http://g.live.com qui transfère un utilisateur vers une page Web correspondant pour télécharger le OSC. Une liaison g OSC se présente sous la forme http://g.live.com/0CR _LCID_/ _Glink_, où _LCID_ et _Glink_ spécifient les paramètres régionaux, la version et le nombre de bits d’Outlook sur l’ordinateur client. Chaque g-lien pointe vers un fichier exécutable et est propre aux valeurs _LCID_ et _Glink_ spécifiés. 
  
Par exemple, le lien-g pour installer la dernière version de l’OSC pour Outlook 2003 ou Outlook 2007 pour le LCID 1033 (US English) est comme suit :
  
http://g.live.com/0CR1033/80
  
Pour plus d’informations sur les valeurs de _Glink_ pour différentes versions et le nombre de bits d’Outlook et les valeurs _LCID_ de paramètres régionaux pris en charge, voir #7 dans la section [Installation Checklist](#olosc_InstallationOverview_InstallationChecklist) ci-dessous. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Liste de vérification d’installation

Le package d’installation de fournisseur doit effectuer une série de vérifications de l’installation, comme le montre la Figure 1, pour s’assurer que le fournisseur s’installe correctement.
  
**La figure 1. Logique d’installation fournisseur**

![Liste de vérification d’installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
La procédure suivante décrit les vérifications d’installation décrites dans la Figure 1.
  
1. Comme condition préalable, détecter si Outlook est installé ou présenter et si installé ou il est présent, ce paramètre détermine si la version d’Outlook prend en charge l’OSC. Pour plus d’informations sur la détection de la version installée d’Outlook, voir [vérifier la Version d’Outlook](http://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Si la version installée d’Outlook est antérieure à Outlook 2003, il est impossible de terminer la procédure d’installation de fournisseur. Informer l’utilisateur pour obtenir une version d’Outlook et la OSC avant de continuer à installer le fournisseur OSC pris en charge.
    
   - Si Outlook n’est pas installé, passez à l’étape 2.
    
   - Si Outlook 2003 ou Outlook 2007 est installé, passez à l’étape 3. 
    
   - Si Outlook 2010 ou Outlook 2013 est installé, passez à l’étape 4.
    
2. **Effectuez cette étape si Outlook n’est pas installé sur l’ordinateur client :**
    
   1. Vérifiez si l’OSC est installé comme un composant par défaut d’une installation de Click-to-Run d’Outlook 2010 ou Outlook 2013. Examiner le `VirtualOutlook` clé à l’emplacement suivant dans le Registre Windows : 
      
      - Pour Outlook 2010`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Pour Outlook Social Connector 2013`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      Le `VirtualOutlook` clé est une valeur REG_SZ qui contient la balise de paramètres régionaux, tel que « en-us », du produit installé. 
      
   2. Si le `VirtualOutlook` clé n’existe pas, Outlook n’est pas présent sur l’ordinateur client et ne pas effectuer la procédure d’installation de fournisseur. Informer l’utilisateur pour obtenir une version d’Outlook et la OSC avant de continuer à installer le fournisseur OSC pris en charge. 
      
   3. Si le `VirtualOutlook` clé n’existe pas, Outlook a été livré par Click-to-Run sur l’ordinateur client. Passez à la version installée de la bibliothèque de type OSC en examinant le `OSCVersion` clé à l’emplacement suivant dans le Registre Windows : 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      La valeur de `OSCVersion` est une chaîne qui spécifie le numéro de version de bibliothèque de types de Socialprovider.dll (par exemple, « 1.0 », « 1.1 » ou « 15 »). 
      
   4. Si `OSCVersion` est « 1.0 », « 1.1 » ou « 15 », une version appropriée de OSC est installée. Passez à l’étape 6 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation de la dernière version de l’OSC. 
      
   5. Dans le cas contraire, `OSCVersion` ne contient pas la valeur attendue. Passez à l’étape 6 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation d’une version appropriée de l’OSC. 
    
3. **Effectuez cette étape si Outlook 2003 ou Outlook 2007 est installé sur l’ordinateur client :**
    
   1. Vérifiez si l’OSC est installé en écrivant un programme d’installation une action personnalisée pour tester l’existence de l’ID du composant complet suivant :
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      L’ID du composant complet est un GUID qui fournit une méthode d’indirection à un niveau, semblable à un pointeur. Pour plus d’informations sur Windows Installer, voir [Introduction à la Documentation de Windows Installer](http://msdn.microsoft.com/library/_msi_roadmap_to_windows_installer_documentation.aspx).
      
   2. Si le composant complet spécifié existe, une version de l’OSC est installée. Passez à l’étape 5 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation de la dernière version de l’OSC.
      
   3. Dans le cas contraire, l’OSC n’est pas installé. Passez à l’étape 6 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation d’une version appropriée de l’OSC.
      
4. **Effectuez cette étape si Outlook 2010 ou Outlook 2013 est installé sur l’ordinateur client :**
    
   1. Déterminer le nombre de bits de la version installée d’Outlook en examinant le `Bitness` clé à l’emplacement suivant dans le Registre Windows : 
      
      - Pour Outlook 2010, consultez`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Pour Outlook 2013, consultez`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      Le `Bitness` clé est « x86 » pour Outlook 32 bits, ou « x64 » pour Outlook 64 bits. 
      
   2. Si votre fournisseur est un fournisseur managé et que vous avez compilé le composant fournisseur spécifiant la plateforme cible en tant que **Tout processeur**, passez à l’étape 6 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation de la dernière version de l’OSC. Votre fournisseur ne fonctionne pas sur les versions 32 bits et 64 bits de l’OSC.
      
   3. Si votre fournisseur est un composant COM natif, examinez le nombre de bits de la version installée d’Outlook :
      
      - Si la version installée d’Outlook est 32 bits, votre procédure d’installation doivent installer un fournisseur de 32 bits (à l’étape 8), après avoir vérifié qu’un OSC approprié est installé.
      
      - Dans le cas contraire, la version installée d’Outlook est 64 bits, et votre procédure d’installation aura installer un fournisseur de 64 bits (à l’étape 8), après avoir vérifié qu’un OSC approprié est installé. 
      
   4. Passez à l’étape 6 pour trouver les paramètres régionaux à interface utilisateur Outlook actif pour préparer l’installation d’une version appropriée de l’OSC.
    
5. **Procéder à cette étape si Outlook 2003 ou Outlook 2007 est installé, et l’OSC est installé sur l’ordinateur client :** Vérifier la régionaux du interface utilisateur Outlook en examinant le `OSCLcid` clé à l’emplacement suivant dans le Registre Windows : 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   Le `OSCLcid` clé est une valeur DWORD qui spécifie la balise de paramètres régionaux Internet Engineering Task Force (IETF) (définie par la [[norme RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)), qui représente les paramètres d’interface utilisateur actuelle Outlook régionaux. Passez à l’étape 7 pour installer le dernier OSC sur l’ordinateur client.
    
6. **Effectuez cette étape si Outlook 2003 ou Outlook 2007 est installé, ou Outlook 2010 ou Outlook 2013 est présent, mais la dernière OSC n’est pas nécessairement installé sur l’ordinateur client :**
    
   Utilisez l’objet **LanguageSettings** pour déterminer le LCID des paramètres régionaux d’interface utilisateur Outlook. L’extrait de code Visual Basic Scripting Edition (VBScript) suivant montre comment obtenir le LCID des paramètres régionaux d’interface utilisateur Outlook. 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **Effectuez cette étape si le programme d’installation a LCID de la version installée d’Outlook, mais la dernière OSC n’est pas nécessairement installé sur l’ordinateur client :**
    
   La chaîne d’un lien de g dans votre package d’installation pour vous assurer que la dernière version de l’OSC est installée sur l’ordinateur client. Le format de liens g est comme suit :
    
   http://g.live.com/0CR_LCID_ /  _Glink_
    
   Reportez-vous au tableau 1 ci-dessous pour les valeurs _LCID_ pris en charge et le tableau 2 pour les valeurs _Glink_ pris en charge. Par exemple, le lien-g pour installer la dernière version de l’OSC 32 bits pour 32 bits Outlook Social Connector 2013 (US English) est comme suit : 
    
   http://g.live.com/0CR1033/82
    
8. Installer le fournisseur. La procédure d’installation fournisseur doit enregistrer l’identificateur programmatique (ProgID) dans l’emplacement de Registre Windows approprié. Pour plus d’informations, voir [enregistrement d’un fournisseur](registering-a-provider.md). En outre, n’oubliez pas que le nombre de bits du fournisseur pour être installée est la même que le nombre de bits de la version d’Outlook présent sur l’ordinateur client. Par exemple, il est recommandé d’installer un fournisseur de 32 bits s’il existe 32 bits Outlook 2013 et un fournisseur de 64 bits si 64-bit Outlook 2013 est installé. Pour Outlook 2003 ou 2007, uniquement la version 32 bits de votre fournisseur s’applique. 
    
**Tableau 1 : Paramètres régionaux pris en charge et les valeurs LCID correspondants au format hexadécimal pour l’OSC**
  
|**Paramètres régionaux**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|CA-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|l’Union européenne-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|général-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kz-kz  <br/> |1087  <br/> |
|ko-ko  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|SR-cyrl-cs  <br/> |3098  <br/> |
|SR-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tableau 2 : Prise en charge des valeurs Glink pour l’OSC**
  
|**Valeur GLINK**|**Fonction**|
|:-----|:-----|
|80  <br/> |Installe la dernière version de OSC pour Outlook 2003 ou Outlook 2007.  <br/> |
|82  <br/> |Installe le dernier correctif de OSC 32 bits d’Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Installe le dernier correctif de OSC 64 bits d’Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Inscription d’un fournisseur](registering-a-provider.md) 
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

