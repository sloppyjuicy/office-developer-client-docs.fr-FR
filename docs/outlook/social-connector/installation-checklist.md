---
title: Liste de vérification d’installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Cette rubrique décrit les conditions préalables à l'installation d'un fournisseur Outlook Social Connector (OSC) et l'installation vérifie que le programme d'installation de votre fournisseur doit se terminer pour fonctionner correctement.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286338"
---
# <a name="installation-checklist"></a>Liste de vérification d’installation

Cette rubrique décrit les conditions préalables à l'installation d'un fournisseur Outlook Social Connector (OSC) et l'installation vérifie que le programme d'installation de votre fournisseur doit se terminer pour fonctionner correctement.
  
## <a name="installation-overview"></a>Présentation de l'installation

Les utilisateurs doivent installer des fournisseurs OSC uniquement si une version de prise en charge d'Outlook est présente et que le OSC est installé et activé sur l'ordinateur client. Les versions de prise en charge d'Outlook sont Office Outlook 2003, Office Outlook 2007, Outlook 2010 et Outlook 2013 (installé sur l'ordinateur client ou, dans le cas d'Outlook 2010 et Outlook 2013, fourni par «démarrer en un clic» sur l'ordinateur client). Pour garantir la réussite de l'installation, le programme d'installation de votre fournisseur doit effectuer les opérations suivantes:
  
- Vérifiez l'existence d'une version prise en charge d'Outlook.
    
- Vérifiez que le OSC est installé.
    
> [!NOTE]
> «Démarrer en un clic» est un environnement virtuel dans lequel Outlook 2010 (32 bits) ou Outlook 2013 (32 bits) peuvent s'exécuter. Pour Outlook 2013, vérifiez si la clé VirtualOutlook existe dans HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook du Registre Windows. Pour plus d'informations sur la remise d'Outlook en tant que produit «démarrer en un clic» sur un ordinateur client, consultez [la rubrique How to verify if Outlook](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx)on a-Run-to-Run Product. 
  
Toutefois, l'utilisateur doit s'assurer que le OSC est activé avant d'installer le fournisseur.
  
Les tiers, y compris les fournisseurs OSC, ne peuvent pas redistribuer OSC. Toutefois, si le OSC n'est pas installé, le programme d'installation du fournisseur peut utiliser les liens g-Links appropriés pour installer le OSC sur l'ordinateur client. Un lien g est une URL spécialement construite sur https://g.live.com qui transfère un utilisateur vers une page Web correspondante pour télécharger OSC. Un OSC g-Link est mis en https://g.live.com/0CR forme en tant que _LCID_/ _Glink_, où _LCID_ et _Glink_ spécifient les paramètres régionaux, la version et le nombre de bits d'Outlook sur l'ordinateur client. Chaque lien g pointe vers un exécutable et est spécifique aux valeurs _LCID_ et _Glink_ spécifiées. 
  
Par exemple, la liaison g-Link pour installer la dernière version du OSC pour Outlook 2003 ou Outlook 2007 pour le LCID 1033 (anglais (États-Unis)) est la suivante:
  
https://g.live.com/0CR1033/80
  
Pour plus d'informations sur les valeurs _Glink_ pour les différentes versions et le nombre de bits d'Outlook, ainsi que sur les valeurs _LCID_ pour les paramètres régionaux pris en charge, consultez #7 dans la [liste de vérification d'installation](#olosc_InstallationOverview_InstallationChecklist) ci-dessous. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Liste de vérification d’installation

Le package d'installation du fournisseur doit effectuer une série de contrôles d'installation, comme illustré à la figure 1, pour s'assurer que le fournisseur s'installe correctement.
  
**Figure 1. Logique d'installation du fournisseur**

![Liste de vérification d’installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
La procédure suivante décrit les vérifications d'installation décrites dans la figure 1.
  
1. Comme condition préalable, détectez si Outlook est installé ou présent, et s'il est installé ou présent, déterminez si la version d'Outlook prend en charge le OSC. Pour plus d'informations sur la détection de la version installée d'Outlook, consultez [la rubrique vérifier la version d'Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Si la version installée d'Outlook est antérieure à Outlook 2003, la procédure d'installation du fournisseur ne peut pas être exécutée. InFormez l'utilisateur pour obtenir une version prise en charge d'Outlook et du OSC avant de procéder à l'installation du fournisseur OSC.
    
   - Si Outlook n'est pas installé, passez à l'étape 2.
    
   - Si Outlook 2003 ou Outlook 2007 est installé, passez à l'étape 3. 
    
   - Si Outlook 2010 ou Outlook 2013 est installé, passez à l'étape 4.
    
2. **Procédez à cette étape si Outlook n'est pas installé sur l'ordinateur client:**
    
   1. Vérifiez si OSC est installé en tant que composant par défaut d'une installation «démarrer en un clic» d'Outlook 2010 ou d'Outlook 2013. Examinez `VirtualOutlook` la clé à l'emplacement suivant dans le Registre Windows: 
      
      - Pour Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Pour Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      La `VirtualOutlook` clé est une valeur REG_SZ qui contient la balise locale, telle que «en-US», du produit installé. 
      
   2. Si la `VirtualOutlook` clé n'existe pas, Outlook n'est pas présent sur l'ordinateur client et la procédure d'installation du fournisseur ne peut pas être exécutée. InFormez l'utilisateur pour obtenir une version prise en charge d'Outlook et du OSC avant de procéder à l'installation du fournisseur OSC. 
      
   3. Si la `VirtualOutlook` clé existe, Outlook a été remis par «démarrer en un clic» sur l'ordinateur client. Vérifiez la version installée de la bibliothèque de types OSC en examinant la `OSCVersion` clé à l'emplacement suivant dans le Registre Windows: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      La valeur de `OSCVersion` est une chaîne qui spécifie le numéro de version de la bibliothèque de types socialprovider. dll (par exemple, «1,0», «1,1» ou «15»). 
      
   4. S' `OSCVersion` il s'agit de "1,0", "1,1" ou "15", une version appropriée de OSC est installée. Passez à l'étape 6 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation de la dernière version du OSC. 
      
   5. Sinon, `OSCVersion` ne contient pas de valeur attendue. Passez à l'étape 6 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation d'une version appropriée du OSC. 
    
3. **Suivez cette étape si Outlook 2003 ou Outlook 2007 est installé sur l'ordinateur client:**
    
   1. Vérifiez si OSC est installé en écrivant une action personnalisée d'installation pour vérifier l'existence de l'ID de composant qualifié suivant:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      L'ID de composant qualifié est un GUID qui fournit une méthode d'indirection à un seul niveau, semblable à un pointeur. Pour plus d'informations sur Windows Installer, consultez [la rubrique Roadmap to Windows Installer documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Si le composant qualifié spécifié existe, une version du OSC est installée. Passez à l'étape 5 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation de la dernière version du OSC.
      
   3. Sinon, OSC n'est pas installé. Passez à l'étape 6 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation d'une version appropriée du OSC.
      
4. **Suivez cette étape si Outlook 2010 ou Outlook 2013 est installé sur l'ordinateur client:**
    
   1. Déterminez le nombre de bits de la version installée d'Outlook `Bitness` en examinant la clé à l'emplacement suivant dans le Registre Windows: 
      
      - Pour Outlook 2010, consultez la page`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Pour Outlook 2013, consultez la page`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      La `Bitness` clé est «x86» pour Outlook 32 bits ou «x64» pour Outlook 64 bits. 
      
   2. Si votre fournisseur est un fournisseur géré et si vous avez compilé le composant fournisseur en spécifiant la plateforme cible comme **n'importe quelle UC**, passez à l'étape 6 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation de la dernière version du OSC. Votre fournisseur fonctionnera sur les versions 32 bits et 64 bits du OSC.
      
   3. Si votre fournisseur est un composant COM natif, examinez le nombre de bits de la version installée d'Outlook:
      
      - Si la version installée d'Outlook est 32 bits, votre procédure d'installation devra installer un fournisseur 32 bits (à l'étape 8), après avoir vérifié qu'un OSC approprié est installé.
      
      - Dans le cas contraire, la version installée d'Outlook est 64 bits et votre procédure d'installation doit installer un fournisseur 64 bits (à l'étape 8), après avoir vérifié qu'un OSC approprié est installé. 
      
   4. Passez à l'étape 6 pour rechercher les paramètres régionaux de l'interface utilisateur Outlook en cours afin de préparer l'installation d'une version appropriée du OSC.
    
5. **Procédez à cette étape si outlook 2003 ou outlook 2007 est installé, et si le OSC est installé sur l'ordinateur client:** Vérifiez les paramètres régionaux de l'interface utilisateur Outlook en examinant la `OSCLcid` clé à l'emplacement suivant dans le Registre Windows: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   La `OSCLcid` clé est une valeur DWORD qui spécifie la balise de paramètres régionaux IETF (Internet Engineering Task Force) (définie par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), qui représente les paramètres régionaux actuels de l'interface utilisateur Outlook. Passez à l'étape 7 pour installer le dernier OSC sur l'ordinateur client.
    
6. **Procédez à cette étape si Outlook 2003 ou Outlook 2007 est installé, ou si Outlook 2010 ou Outlook 2013 est présent, mais que le dernier OSC n'est pas nécessairement installé sur l'ordinateur client:**
    
   Utilisez l'objet **LanguageSettings** pour déterminer le LCID des paramètres régionaux de l'interface utilisateur d'Outlook. L'extrait de code Visual Basic Scripting Edition (VBScript) suivant montre comment obtenir le LCID des paramètres régionaux de l'interface utilisateur d'Outlook. 
    
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

7. **Procédez à cette étape si le programme d'installation a le LCID de la version installée d'Outlook, mais le dernier OSC n'est pas nécessairement installé sur l'ordinateur client:**
    
   EnChaînez un lien g-Link dans votre package d'installation afin de vous assurer que la dernière version du fichier OSC est installée sur l'ordinateur client. Le format g-Link est le suivant:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   RePortez-vous au tableau 1 ci-dessous pour obtenir les valeurs _LCID_ prises en charge et le tableau 2 pour les valeurs _Glink_ prises en charge. Par exemple, le lien g-Link pour installer la dernière version de l' 32 bits OSC pour Outlook Social Connector 2013 32 bits (anglais (États-Unis)) est le suivant: 
    
   https://g.live.com/0CR1033/82
    
8. Installez le fournisseur. La procédure d'installation du fournisseur doit enregistrer l'identificateur programmatique (ProgID) dans l'emplacement du Registre Windows approprié. Pour plus d'informations, consultez [la rubrique Registering a Provider](registering-a-provider.md). Assurez-vous également que le nombre de bits du fournisseur à installer est le même que le nombre de bits de la version d'Outlook présente sur l'ordinateur client. Par exemple, installez un fournisseur de 32 bits si Outlook 2013 32 bits est présent, et un fournisseur de 64 bits si Outlook 64 bits est installé. Pour Outlook 2003 ou 2007, seule la version 32 bits de votre fournisseur s'applique. 
    
**Tableau 1: paramètres régionaux pris en charge et valeurs LCID correspondantes en hexadécimal pour le OSC**
  
|**Paramètres régionaux**|**LCID**|
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
|SR-Cyrl-CS  <br/> |3098  <br/> |
|SR-LATN-CS  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tableau 2: valeurs Glink prises en charge pour le OSC**
  
|**Valeur Glink**|**Fonction**|
|:-----|:-----|
|80  <br/> |Installe la dernière version de OSC pour Outlook 2003 ou Outlook 2007.  <br/> |
|82  <br/> |Installe le correctif le plus récent de la version 32 bits OSC pour Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Installe le correctif le plus récent de la version 64 bits OSC pour Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Inscription d'un fournisseur](registering-a-provider.md) 
- [Étapes rapides pour apprendre à développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)

