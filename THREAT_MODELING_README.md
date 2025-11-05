# Advanced Threat Modeling Platform

A comprehensive threat modeling platform with file-based workflow, interactive D3.js visualizations, CVSS v3.1 scoring, and AI-powered threat intelligence.

## Features

### 🚀 No Database Required
- **File-Based Workflow**: All data is managed through JSON file uploads and downloads
- **No MongoDB Dependencies**: Completely removed database overhead
- **Portable**: Easy to share and version control threat models

### 📤 File Upload Interface
- **Streamlit Integration**: Modern, user-friendly file upload interface
- **JSON Format**: Simple, standardized attack tree data format
- **Sample Data**: Includes example attack tree for quick start

### 🌳 Interactive D3.js Visualization
- **Draggable Nodes**: Rearrange the tree layout with drag-and-drop (client-side)
- **Click-to-Select**: Click nodes to view detailed information in side panel
- **Hover Tooltips**: Quick CVSS scores and metrics on hover
- **Zoom & Pan**: Navigate large attack trees easily
- **Path Filtering**: Filter nodes by severity level (Critical/High/Medium/Low)
- **Severity Highlighting**: Color-coded nodes based on threat severity
- **Critical Path**: Highlight the most dangerous attack paths
- **Reset Layout**: Restore original tree structure with one click

### 📊 CVSS v3.1 Scoring
- **Complete Calculator**: Full CVSS v3.1 base score calculation
- **Interactive Form**: Easy-to-use metric selection
- **Severity Ratings**: Automatic severity classification (None/Low/Medium/High/Critical)
- **Vector String**: Generate CVSS vector strings for documentation

### 🤖 Perplexity AI Integration
- **Threat Analysis**: AI-powered threat intelligence and analysis
- **Mitigation Strategies**: Get AI-generated mitigation recommendations
- **Real-time Intelligence**: Online threat intelligence using Perplexity's Sonar models

## Installation

```bash
# Install dependencies
pip install -r requirements.txt

# Run Jupyter notebook (for development)
jupyter notebook REU1.ipynb

# Or run standalone Streamlit app (extract code from notebook first)
streamlit run app.py
```

## Quick Start

1. **Open the Notebook**: Launch `REU1.ipynb` in Jupyter
2. **Run All Cells**: Execute all cells to load the application
3. **Configure API Key** (Optional): Add your Perplexity API key in the sidebar for AI features
4. **Upload Attack Tree**: Use the Upload tab to load your attack tree JSON file
   - Or download and use the included `example_attack_tree.json`
5. **Visualize**: Navigate to the Visualization tab to explore the interactive tree
6. **Analyze**: Use the Analysis tab to view statistics and export data
7. **AI Intelligence**: Get AI-powered insights and mitigations (requires API key)
8. **Calculate CVSS**: Use the CVSS Calculator for new threats

## Attack Tree JSON Format

```json
{
  "name": "Root Attack",
  "description": "Main attack objective",
  "cvss_score": 9.8,
  "severity": "Critical",
  "attack_vector": "Network",
  "likelihood": "High",
  "impact": "High",
  "children": [
    {
      "name": "Sub Attack 1",
      "description": "First attack vector",
      "cvss_score": 8.5,
      "severity": "High",
      "attack_vector": "Network",
      "likelihood": "Medium",
      "impact": "High",
      "children": []
    }
  ]
}
```

## Visualization Controls

- **Drag Nodes**: Click and drag any node to reposition it
- **Zoom**: Use mouse wheel or pinch gesture to zoom in/out
- **Pan**: Click and drag on empty space to pan the view
- **Select Node**: Click on a node to see details in the side panel
- **Filter**: Use the severity dropdown to filter by threat level
- **Highlight Critical Path**: Click button to highlight high-risk attack paths
- **Reset Layout**: Click to restore the original tree structure
- **Reset Zoom**: Click to reset zoom level to default

## Technical Details

### Technologies Used
- **Streamlit**: Modern Python web framework for data apps
- **D3.js v7**: JavaScript library for interactive visualizations
- **Pandas**: Data analysis and manipulation
- **NumPy**: Numerical computing
- **Requests**: HTTP library for API calls

### CVSS v3.1 Implementation
The platform implements the complete CVSS v3.1 specification:
- Base Score calculation with all metrics
- Impact Sub Score (ISS) calculation
- Exploitability calculation
- Scope changes handling
- Accurate severity ratings

### Perplexity AI Integration
- Uses Perplexity's Sonar model for online threat intelligence
- Real-time analysis of security threats
- Context-aware mitigation recommendations
- Requires API key from perplexity.ai

## File-Based Workflow Benefits

1. **No Database Setup**: No MongoDB or database installation required
2. **Version Control**: Track changes to threat models with Git
3. **Easy Sharing**: Share JSON files via email, Slack, or any file system
4. **Portability**: Run anywhere Python and Streamlit are available
5. **Backup & Recovery**: Simple file-based backups
6. **Collaboration**: Multiple team members can work on different threat models

## Use Cases

- **Security Assessments**: Model potential attack scenarios
- **Risk Analysis**: Calculate and prioritize security risks
- **Penetration Testing**: Plan and document attack paths
- **Compliance**: Document security posture for audits
- **Training**: Teach security concepts with interactive visualizations
- **Red Team Planning**: Visualize and plan attack scenarios
- **Blue Team Defense**: Understand attack patterns for better defense

## API Key Setup

To use AI features:

1. Sign up at [perplexity.ai](https://www.perplexity.ai/)
2. Generate an API key from your dashboard
3. Enter the API key in the sidebar of the Streamlit app
4. AI features will become available immediately

## Example Usage

See `example_attack_tree.json` for a complete example of a web application attack scenario including:
- SQL Injection attacks
- Cross-Site Scripting (XSS) vectors
- Brute force attacks
- Multiple severity levels
- Complete CVSS scoring

## Contributing

This is a threat modeling platform designed for security professionals. Contributions welcome!

## License

This project is provided as-is for educational and professional use.

## Support

For issues or questions, please refer to the inline documentation in the notebook.
