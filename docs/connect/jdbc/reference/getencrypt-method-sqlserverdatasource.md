---
title: GetEncrypt-Methode (SQLServerDataSource) | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: jdbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
apiname: getEncrypt Method (SQLServerDataSource)
apilocation: getEncrypt Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 1cdb12dd-6e6f-4bbd-8f5f-9e630f3ee2c9
caps.latest.revision: "19"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: cb76a00e1fdf8b2999675bc1949e8cc06ff25d9b
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2017
---
# <a name="getencrypt-method-sqlserverdatasource"></a>getEncrypt-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt eine **booleschen** -Wert, der angibt, ob die Encrypt-Eigenschaft aktiviert ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean getEncypt()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 **"true"** Wenn verschlüsseln aktiviert ist. Andernfalls lautet der Wert **false**.  
  
## <a name="remarks"></a>Hinweise  
 Wenn die Encrypt-Eigenschaft, um festgelegt wird **"true"**, [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] wird sichergestellt, dass [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] verwendet SSL-Verschlüsselung für alle Daten, die zwischen dem Client und dem Server gesendet werden, wenn der Server ein Zertifikat installiert ist.  
  
 Wenn die Encrypt-Eigenschaft nicht angegeben ist, oder legen Sie auf **"false"**, der Treiber erzwingt nicht die [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] SSL-Verschlüsselung unterstützt. Wenn die [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] Instanz nicht zum Erzwingen der SSL-Verschlüsselung konfiguriert ist, eine Verbindung ohne Verschlüsselung hergestellt. Wenn die [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] Instanz ist so konfiguriert, dass das Erzwingen der SSL-Verschlüsselung, die [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] wird automatisch SSL-Verschlüsselung aktivieren, bei der Ausführung auf einer ordnungsgemäß konfigurierten Java Virtual Machine (JVM), da andernfalls die Verbindung wird beendet, und der Treiber löst einen Fehler. Wenn die Verschlüsselungseigenschaft nicht festgelegt ist, die [GetEncrypt](../../../connect/jdbc/reference/getencrypt-method-sqlserverdatasource.md) Methodenrückgabe den Standardwert von **"false"**.  
  
## <a name="see-also"></a>Siehe auch  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
