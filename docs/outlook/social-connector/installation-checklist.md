---
title: Liste de vérification d’installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Cette rubrique décrit les conditions préalables à l’installation réussie d’un fournisseur Outlook Social Connector (OSC) et les vérifications d’installation que votre programme d’installation doit effectuer pour fonctionner correctement.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286338"
---
# <a name="installation-checklist"></a>Liste de vérification d’installation

Cette rubrique décrit les conditions préalables à l’installation réussie d’un fournisseur Outlook Social Connector (OSC) et les vérifications d’installation que votre programme d’installation doit effectuer pour fonctionner correctement.
  
## <a name="installation-overview"></a>Vue d’ensemble de l’installation

Les utilisateurs doivent installer les fournisseurs OSC uniquement si une version de prise en charge de Outlook est présente et que l’OSC est installé et activé sur l’ordinateur client. Les versions de prise en charge de Outlook sont Office Outlook 2003, Office Outlook 2007, Outlook 2010 et Outlook 2013 (installées sur l’ordinateur client ou, dans le cas de Outlook 2010 et Outlook 2013, livrées par Click-to-Run sur l’ordinateur client). Pour garantir la réussite de l’installation, votre programme d’installation de fournisseur doit :
  
- Vérifiez si une version prise en charge de Outlook est présente.
    
- Vérifiez si l’OSC est installé.
    
> [!NOTE]
> Click-to-Run est un environnement virtuel dans lequel Outlook 2010 (32 bits) ou Outlook 2013 (32 bits) peut s’exécuter. Pour Outlook 2013, vérifiez si la clé VirtualOutlook existe dans HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook du Registre Windows. Pour plus d’informations sur la livraison de Outlook en tant que produit « En un clic » sur un ordinateur client, voir Comment vérifier si Outlook est disponible sur un ordinateur en tant que produit « [Click-to-Run](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)». 
  
Toutefois, l’utilisateur doit s’assurer que l’OSC est activé avant d’installer le fournisseur.
  
Les tiers, y compris les fournisseurs OSC, ne peuvent pas redistribuer l’OSC. Toutefois, si OSC n’est pas installé, le programme d’installation du fournisseur peut utiliser les liens g appropriés pour installer OSC sur l’ordinateur client. Un lien g est une URL spécialement construite sur qui permet à un utilisateur de se rendre sur une page web correspondante https://g.live.com pour télécharger OSC. Un lien G OSC est au format https://g.live.com/0CR _LCID_ /  _Glink,_ où _LCID_ et _Glink_ spécifient les paramètres régionaux, la version et le nombre de bits de Outlook sur l’ordinateur client. Chaque liaison g pointe vers un exécutable et est spécifique aux valeurs  _LCID_ et  _Glink_ spécifiées. 
  
Par exemple, le lien g pour installer la dernière version d’OSC pour Outlook 2003 ou Outlook 2007 pour le LCID 1033 (anglais des États-Unis) est le suivant :
  
https://g.live.com/0CR1033/80
  
Pour plus d’informations sur les valeurs _Glink_ pour différentes versions et le nombre de bits de Outlook, ainsi que sur les valeurs _LCID_ pour les paramètres régionaux pris en charge, voir #7 dans la section [Installation Checklist](#olosc_InstallationOverview_InstallationChecklist) ci-dessous. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Liste de vérification d’installation

Le package d’installation du fournisseur doit effectuer une série de vérifications d’installation, comme le montre la figure 1, pour s’assurer que le fournisseur s’installe correctement.
  
**Figure 1. Logique d’installation du fournisseur**

![Liste de vérification d’installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
La procédure suivante décrit les vérifications d’installation décrites dans la figure 1.
  
1. En tant que condition préalable, déterminez si Outlook est installé ou présent, et s’il est installé ou présent, déterminez si la version de Outlook prend en charge OSC. Pour plus d’informations sur la détection de la version installée de Outlook, voir Vérifier la [version de Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Si la version installée de Outlook est antérieure à Outlook 2003, la procédure d’installation du fournisseur ne peut pas se terminer. Informez l’utilisateur pour obtenir une version prise en charge de Outlook osc avant de poursuivre l’installation du fournisseur OSC.
    
   - Si Outlook n’est pas installé, passer à l’étape 2.
    
   - Si Outlook 2003 ou Outlook 2007 est installé, passer à l’étape 3. 
    
   - Si Outlook 2010 ou Outlook 2013 est installé, passer à l’étape 4.
    
2. **Procédez à cette étape si Outlook n’est pas installé sur l’ordinateur client :**
    
   1. Vérifiez si OSC est installé comme composant par défaut d’une installation « En un clic » de Outlook 2010 ou Outlook 2013. Examinez `VirtualOutlook` la clé à l’emplacement suivant dans Windows registre : 
      
      - Pour Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Pour Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      La clé est une valeur REG_SZ qui contient la balise locale, telle que «  `VirtualOutlook` en-us », du produit installé. 
      
   2. Si la `VirtualOutlook` clé n’existe pas, Outlook n’est pas présent sur l’ordinateur client et la procédure d’installation du fournisseur ne peut pas se terminer. Informez l’utilisateur pour obtenir une version prise en charge de Outlook osc avant de poursuivre l’installation du fournisseur OSC. 
      
   3. Si la `VirtualOutlook` clé existe, Outlook a été remis par Click-to-Run sur l’ordinateur client. Vérifiez la version installée de la bibliothèque de types OSC en examinant la clé à l’emplacement suivant dans Windows `OSCVersion` registre : 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      La valeur est une chaîne qui spécifie le numéro de version de bibliothèque de types de  `OSCVersion` Socialprovider.dll (par exemple, « 1.0 », « 1.1 » ou « 15 »). 
      
   4. Si la version  `OSCVersion` est « 1.0 », « 1.1 » ou « 15 », une version appropriée d’OSC est installée. Passer à l’étape 6 pour trouver les paramètres régionaux Outlook’interface utilisateur actuelle pour préparer l’installation de la dernière version d’OSC. 
      
   5. Dans le cas  `OSCVersion` contraire, ne contient pas de valeur attendue. Passer à l’étape 6 pour rechercher les paramètres régionaux Outlook’interface utilisateur actuelle pour préparer l’installation d’une version appropriée d’OSC. 
    
3. **Procédez comme cela si Outlook 2003 ou Outlook 2007 est installé sur l’ordinateur client :**
    
   1. Vérifiez si l’OSC est installé en écrivant une action personnalisée de programme d’installation pour tester l’existence de l’ID de composant qualifié suivant :
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      L’ID de composant qualifié est un GUID qui fournit une méthode d’indirection à un seul niveau, semblable à un pointeur. Pour plus d’informations sur Windows installer, voir la feuille de [route Windows documentation du programme d’installation.](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)
      
   2. Si le composant qualifié spécifié existe, une version de l’OSC est installée. Passer à l’étape 5 pour rechercher les paramètres régionaux Outlook’interface utilisateur actuelle pour préparer l’installation de la dernière version d’OSC.
      
   3. Sinon, l’OSC n’est pas installé. Passer à l’étape 6 pour rechercher les paramètres régionaux Outlook’interface utilisateur actuelle pour préparer l’installation d’une version appropriée d’OSC.
      
4. **Procédez comme cela si Outlook 2010 ou Outlook 2013 est installé sur l’ordinateur client :**
    
   1. Déterminez le nombre de bits de la version installée de Outlook en examinant la clé à l’emplacement suivant dans Windows `Bitness` registre : 
      
      - Pour Outlook 2010, voir`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Pour Outlook 2013, voir`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      La clé est « x86 » pour les Outlook 32 bits ou « x64 » pour les Outlook `Bitness` 64 bits. 
      
   2. Si votre fournisseur est un fournisseur géré et que vous avez compilé le composant fournisseur en spécifiant la plateforme cible comme toute UC, procédez à l’étape 6 pour rechercher les paramètres régionaux actuels de l’interface utilisateur Outlook afin de préparer l’installation de la dernière version d’OSC. Votre fournisseur fonctionne sur les versions 32 bits et 64 bits de l’OSC.
      
   3. Si votre fournisseur est un composant COM natif, examinez le nombre de bits de la version installée de Outlook :
      
      - Si la version installée de Outlook est 32 bits, votre procédure d’installation doit installer un fournisseur 32 bits (à l’étape 8), après avoir garanti qu’un OSC approprié est installé.
      
      - Dans le cas contraire, la version installée de Outlook est 64 bits et votre procédure d’installation devra installer un fournisseur 64 bits (à l’étape 8), après s’être assuré qu’un OSC approprié est installé. 
      
   4. Procédez à l’étape 6 pour rechercher les paramètres régionaux Outlook’interface utilisateur actuelle afin de préparer l’installation d’une version appropriée d’OSC.
    
5. **Continuez cette étape si Outlook 2003 ou Outlook 2007** est installé et que l’OSC est installé sur l’ordinateur client : Vérifiez les paramètres régionaux Outlook’interface utilisateur actuelle en examinant la clé à l’emplacement suivant dans `OSCLcid` Windows registre : 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   La clé est une valeur DWORD qui spécifie la balise de paramètres régionaux `OSCLcid` IETF (Internet Engineering Task Force) (définie par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), qui représente les paramètres régionaux actuels de l’interface utilisateur Outlook. Procédez à l’étape 7 pour installer la dernière version d’OSC sur l’ordinateur client.
    
6. **Continuez cette étape si Outlook 2003 ou Outlook 2007 est installé, ou Outlook 2010 ou Outlook 2013 est présent, mais que la dernière version d’OSC n’est pas nécessairement installée sur l’ordinateur client :**
    
   Utilisez **l’objet LanguageSettings** pour déterminer le LCID des paramètres régionaux Outlook’interface utilisateur. L’extrait de code Visual Basic Scripting Edition (VBScript) montre comment obtenir le LCID des paramètres régionaux Outlook’interface utilisateur. 
    
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

7. **Continuez cette étape si le programme d’installation possède le LCID de la version installée de Outlook, mais que le dernier OSC n’est pas nécessairement installé sur l’ordinateur client :**
    
   Chaînez un lien g dans votre package d’installation pour vous assurer que la dernière version d’OSC est installée sur l’ordinateur client. Le format de liaison g est le suivant :
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   Reportez-vous au tableau 1 ci-dessous pour les valeurs  _LCID_ pris en charge et au tableau 2 pour les valeurs  _Glink pris_ en charge. Par exemple, le lien g pour installer la dernière version d’OSC 32 bits pour Outlook Social Connector 2013 (États-Unis) est le suivant : 
    
   https://g.live.com/0CR1033/82
    
8. Installez le fournisseur. La procédure d’installation du fournisseur doit inscrire l’identificateur programmatique (ProgID) à l’emplacement Windows registre approprié. Pour plus d’informations, voir [Inscription d’un fournisseur.](registering-a-provider.md) Assurez-vous également que le nombre de bits du fournisseur à installer est identique au nombre de bits de la version de Outlook présente sur l’ordinateur client. Par exemple, installez un fournisseur 32 bits si Outlook 2013 32 bits est présent et un fournisseur 64 bits si Outlook 2013 64 bits est installé. Pour Outlook 2003 ou 2007, seule la version 32 bits de votre fournisseur s’applique. 
    
**Tableau 1 : Paramètres régionaux pris en charge et valeurs LCID correspondantes en hexadécimal pour OSC**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|fr  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kz-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
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
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tableau 2 : Valeurs Glinks pris en charge pour OSC**
  
|**Valeur Glink**|**Fonction**|
|:-----|:-----|
|80  <br/> |Installe la dernière version d’OSC pour Outlook 2003 ou Outlook 2007.  <br/> |
|82  <br/> |Installe le dernier correctif d’OSC 32 bits pour Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Installe le dernier correctif d’OSC 64 bits pour Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Inscription d’un fournisseur](registering-a-provider.md) 
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

